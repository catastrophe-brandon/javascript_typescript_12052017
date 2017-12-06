# Async Notes/Discussion 

Web browsers have
- JS Engine
- DOM
- Networking
- Timers

JS primarily delegates responsibiity to the browser, written in C++

NodeJS - V8 JS engine.
- Process module
- Networking module

JS is single-threaded by definition

### Webworkers

- Browser UI thread is shared with JS
- Modern browsers support WebWOrkers - additional instances of JS.
- WebWorkers can't talk to the DOM, but can use network APIs.
- WebWorkers communicate via IPC-like API.

JS modules are multi-threaded. Only thing single-threaded is JS execution.

### Scenario

Multi-threaded server
1. Request comes in
2. JS receives it
3. Hands off to the file system
 
## Task Execution In Javascript

There's a queue
Tasks build up in the queue (FIFO)
JS has an event loop.
Iterates over tasks and schedules for processor execution.
JS runs task to completion without regard to length of completion.
JS does not run other tasks.
Rule of thumb: tasks should run in < 5ms.

Where do tasks come from?

Example: 
1. Button w/ click event.
2. Click button.
3. Invokes function, task created.

 Tasks are the result of creation of an async operation (function call).
 
 Generally: Function call == Event Created and added to queue.

## UI/JS Sequence Diagram

[Link to image goes here]()

    x = 2;
    $.ajax(---, callback_function{
      // do something with x
      });
      
Behind the scenes this invokes the XHR object.
  1. request made to rest service
  2. rest service responds
  3. callback_function is pushed onto event queue and executed.
  

### Closure 

Purpose: To facilitate communication between async tasks.

Basically pointing to a variable outside the scope of the function. 
Function actually references variable defined on the heap and not a copy.

Function call => Stack Frame - x is defined on stack frame => Callback function stackframe points to caller's stack frame.

Stackframe loading is expensive because it may involve I/O. 
Commonly used because it's intuitive, but it's perf intensive.





