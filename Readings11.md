# Event Driven Programming

## Overview
   Whenever you interact with a webpage, you're creating events. When you click on a button, EVENT! When you press a key, EVENT! These events have associated functions that execute to make a change to the interface in some way.
   
   - Event Driven Programming uses the following concepts:
        - Event Handlers (callback function): will be called with an event is triggered
        - A Main Loop: this listens for event triggers & calls associated event handler for event.

## EventEmitter
   - Node.js provides a module called EventEmitter.
        - Allows the incorporation of Event-Driven-Programming.
        - Checkout [EventEmitter2](https://github.com/EventEmitter2/EventEmitter2) & [EventEmitter3](https://github.com/primus/eventemitter3)

## Object Oriented Programming + Event Driven Programming
   - Object Oriented approach promotes the idea that all behavior of a single unit to be handled from code from that specific unit.
   - We can make use of Event Driven Programming by registering event listeners that will reverse the flow of communication between objects.
        - Rather than needing to reach inside another object to trigger a function, instead we can just emit events and whichever objects are listening to that event will process it how they have been told to.


Resource: [Node Events](https://nodejs.org/api/events.html)

