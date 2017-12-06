# Promises

A hack to implement order of execution between async tasks.

Event loop has MORE THAN ONE QUEUE!

JS Engine comes with two queues. 2nd queues is for promise-related tasks.
Promise queue is a higher-priority queue than normal tasks.

Browsers typically only have 2 queues, but Node has 4 queues.

1. I/O Task queues
2. Set immediate tasks
3. Normal Events
4. Promise-related queues (higher-priority)

Promises added to the language in 2015.

Promise API hides all the closures so we can avoid the pyramid of doom. 
By wrapping async operations.
Promises remove the need of lexical scope and closures by moving it into the promise API.

[Promise anti-patterns](https://github.com/petkaantonov/bluebird/wiki/Promise-anti-patterns)

Catch automatically returns a resolved promise unless there's some sort of a rejection.

ES2017 - async and await uses generators and promises to build yet another layer of abstraction
