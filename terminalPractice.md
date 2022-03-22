# Terminal Practice
  * Notice: all notes taken are from [Ryans Tutorials](https://ryanstutorials.net/linuxtutorial/commandline.php)

## The Command Line
  - What are they?
    - A command line, or terminal, is a text based interface to the system. You are able to enter commands by typing them on the keyboard and feedback will be given to you similarly as text
![one](https://user-images.githubusercontent.com/84699682/159515143-ccd5d492-4373-4c25-ab6a-3b4cf1932f07.JPG)
      - Line 1 presents us with a prompt ( user@bash ). After that we entered a command ( ls ). Typically a command is always the first thing you type. After that we have what are referred to as command line arguments ( -l /home/ryan ). Important to note, these are separated by spaces (there must be a space between the command and the first command line argument also). The first command line argument ( -l ) is also referred to as an option. Options are typically used to modify the behaviour of the command. Options are usually listed before other arguments and typically start with a dash ( - ).
      - Lines 2 - 5 are output from running the command. Most commands produce output and it will be listed straight under the issuing of the command. Other commands just perform their task and don't display any information unless there was an error.
      - Line 6 presents us with a prompt again. After the command has run and the terminal is ready for you to enter another command the prompt will be displayed. If no prompt is displayed then the command may still be running (you will learn later how to deal with this).
Your terminal probably won't have line numbers on it. I have just included them here to make it easier to refer to different parts of the material.

#### Tips:
  - Finding the Terminal
      - If you're on a Mac then you'll find the program Terminal under Applications -> Utilities. An easy way to get to it is the key combination 'command + space' which will bring up Spotlight, then start typing Terminal and it will soon show up.
      - If on Linux then you will probably find it in Applications -> System or Applications -> Utilities. Alternatively you may be able to 'right-click' on the desktop and there may be an option 'Open in terminal'.
  - The check which shell you are using, you may use the 'echo' command. It should print something on the screen that ends with bash.

## Basic Navigation
  - Commands that will help out in navigating
    - pwd: Print Working Directory
    - ls: List the contents of the directory
    - ls -a : Lists the contents of the directory, to include any hidden files
    - cd: Change Directory
    - man : will open up a manual to explain every command available on your system
    - man -k : allows to search the manual by keyword
    - q : Command used to quit manual pages

  - Absolute vs Relative Paths
    - Absolute paths specify a location (file or directory) in relation to the root directory. You can identify them easily as they always begin with a forward slash ( / )
    - Relative paths specify a location (file or directory) in relation to where we currently are in the system. They will not begin with a slash.

## More About Files
  - Under the hood, everything is a file.
  - Types of files:
    - file.exe : executable file / program
    - file.txt : file containing plain text
    - file.png/jpg/gif : these three are different image files.

*NOTE: Linux is case sensitive in terms of the file name. However the file type 
![two](https://user-images.githubusercontent.com/84699682/159517687-9b4ed8bd-8cc0-43fd-a0bb-aa4b3f3e4644.JPG)

## Manual Pages
  - What are Manual Pages?
    - The manual pages are a set of pages that explain every command available on your system including what they do, the specifics of how you run them and what command line arguments they accept.
    - It is possible to do a keyword search on the Manual pages. This can be helpful if you're not quite sure of what command you may want to use but you know what you want to achieve.
    - If you want to search within a manual page this is also possible. To do this, whilst you are in the particular manual page you would like to search press forward slash '/' followed by the term you would like to search for and hit 'enter' If the term appears multiple times you may cycle through them by pressing the 'n' button for next.

## File Manipulation
  | mkdir | rmdir | touch |  cp   |  mv   |  rm   |
  | ----- | ----- | ----- | ----- | ----- | ----- |
  | Make Directory - ie. Create a directory. | Remove Directory - ie. Delete a directory. | Create a blank file. | Copy - ie. Copy a file or directory. | Move - ie. Move a file or directory (can also be used to rename). | Remove - ie. Delete a file. |
  
  *NOTE: The Linux command line does not have an undo feature. Perform destructive actions carefully.
