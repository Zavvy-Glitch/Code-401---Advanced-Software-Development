# Authentication

1. Explain what a "Singleton" is (in Computer Science terms)
    - is a software design pattern that restricts the instantiation of a class to one "single" instance. This is useful when exactly one object is needed to coordinate actions across the system.

2. Explain how the Singleton pattern can be used with Node modules, specifically with classes
    - create a class constructor that can check for an instance that may have already been instantiated. If none exist, instantiate the new instance.

3. If you were tasked with building a middleware system like Express uses, what approach might you take to construct/operate it?
    - middleware? Like a logger file? One that can track ReSTful requests made across a server? Otherwise, I'm not particularly sure how to build my own middleware.

## TERMS

| Router Middleware | Dynamic Module Loading | Singleton Pattern | CRUD -> REST Method Matchs | Mock Testing |
| ----------------- | ---------------------- | ----------------- | -------------------------- | ------------ |
| Denoting HTTP requests `GET`,`POST`,`DELETE`,`PUT`, Router middleware is used to manage those requests | a mechanism by which a computer program can, at run time, load a library (or other binary) into memory, retrieve the addresses of functions and variables contained in the library, execute those functions or access those variables, and unload the library from memory | is a software design pattern that restricts the instantiation of a class to one "single" instance. This is useful when exactly one object is needed to coordinate actions across the system. The term comes from the mathematical concept of a singleton | `Create` -> `POST` \ `Read` -> `GET` \ `Update` -> `PUT`/`PATCH` \ `Delete` -> `DELETE` possibly `DESTROY` | Creating a fake version of an external or internal service that can stand in for the real one, helping your tests run more quickly and more reliably. When your implementation interacts with an object's properties, rather than its function or behavior, a mock can be used |
