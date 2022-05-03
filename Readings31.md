# Context API

What is it?
  - Provides a way to pass data through the component tree without having to pass props down manually at every level
    - Typically React applications have you pass data from the top down by use of props
    - Context provides a way to share values between components without explicitly passing props through every level

When to use Context
  - Designed to share data that is considered to be "global"
    - Example Below (threads `theme` through a prop:
      ``` javascript
      class App extends React.Component {
        render() {
          return <Toolbar theme="dark" />;
        }
      }

      function Toolbar(props) {
        // The Toolbar component must take an extra "theme" prop
        // and pass it to the ThemedButton. This can become painful
        // if every single button in the app needs to know the theme
        // because it would have to be passed through all components.
        return (
          <div>
            <ThemedButton theme={props.theme} />
          </div>
        );
      }

      class ThemedButton extends React.Component {
        render() {
          return <Button theme={this.props.theme} />;
        }
      }
      ```
    - Alternative Example using Context:
      ```javascript
      // Context lets us pass a value deep into the component tree
      // without explicitly threading it through every component.
      // Create a context for the current theme (with "light" as the default).
      const ThemeContext = React.createContext('light');

      class App extends React.Component {
        render() {
          // Use a Provider to pass the current theme to the tree below.
          // Any component can read it, no matter how deep it is.
          // In this example, we're passing "dark" as the current value.
          return (
            <ThemeContext.Provider value="dark">
              <Toolbar />
            </ThemeContext.Provider>
          );
        }
      } 

      // A component in the middle doesn't have to
      // pass the theme down explicitly anymore.
      function Toolbar() {
        return (
          <div>
            <ThemedButton />
          </div>
        );
      }

      class ThemedButton extends React.Component {
        // Assign a contextType to read the current theme context.
        // React will find the closest theme Provider above and use its value.
        // In this example, the current theme is "dark".
        static contextType = ThemeContext;
        render() {
          return <Button theme={this.context} />;
        }
      }
      ```
      
Before deciding to use Context:
  - Context is mainly used with data needs to be accessed by multiple components at varying nested levels
  - Apply sparingly as it makes components difficult to reuse
    - **If you only want to avoid passing some props through many levels, component composition is often a simpler solution than context**
    - There's a bit of redundency passing down props
    - Example below, you see `user` and `avatarSize` props being sent down from the top to each intermediate level:
      ``` javascript
      <Page user={user} avatarSize={avatarSize} />
      // ... which renders ...
      <PageLayout user={user} avatarSize={avatarSize} />
      // ... which renders ...
      <NavigationBar user={user} avatarSize={avatarSize} />
      // ... which renders ...
      <Link href={user.permalink}>
        <Avatar user={user} size={avatarSize} />
      </Link>
      ```
    - Consider this instead, where you can pass down the entire component
      ``` javascript
      function Page(props) {
        const user = props.user;
        const userLink = (
          <Link href={user.permalink}>
            <Avatar user={user} size={props.avatarSize} />
          </Link>
        );
        return <PageLayout userLink={userLink} />;
      }

      // Now, we have:
      <Page user={user} avatarSize={avatarSize} />
      // ... which renders ...
      <PageLayout userLink={...} />
      // ... which renders ...
      <NavigationBar userLink={...} />
      // ... which renders ...
      {props.userLink}
      ```
      
## Context API - Behaviors

  - `React.createContext()` : <- this creates a Context Object. When react renders a component that uses this Context object, it will read the current context value from the closest matching `Provider` above it in the tree
    - Example:
      ``` javascript
      const MyContext = React.createContext(defaultValue);
      ```
  - `Context.Provider()` : <- this allows consuming components to subscribe to context changes
  - *NOTE: Provider components accept a `value` property that will be passed to consuming components / decendants of this provider. One provider can be connected to many consumers. 
    - Example:
      ``` javascript
      <MyContext.Provider value={/* some value */}>
      ```
      
  - Caveats
    - Unintentional renders may be triggered in consumers when a provider's parent re-renders.  
      - Example: rerenders all consumers every time the Provider re-renders because a new object is createad for value
        ``` javascript
        class App extends React.Component {
          render() {
            return (
              <MyContext.Provider value={{something: 'something'}}>
               <Toolbar />
             </MyContext.Provider>
           );
          }
        }
        ```
       - Example: To Fix this, you'll need to lift the value into the Parent's state
          ``` javascript
          class App extends React.Component {
            constructor(props) {
             super(props);
              this.state = {
               value: {something: 'something'},
              };
            }

            render() {
              return (
                <MyContext.Provider value={this.state.value}>
                  <Toolbar />
               </MyContext.Provider>
             );
            }
          }
          ```
