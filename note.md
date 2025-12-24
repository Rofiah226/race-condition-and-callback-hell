# Race Condition


A **race condition** is when two or more things try to use or change the same data at the same time, and the final result depends on who finishes first. 

 It happens when multiple processes or threads access shared data at the same time, and the outcome depends on the timing of their execution.


It is called a race because;
- The processes are __racing__ to finish first
- The winner affects the final result

Race conditions happens a lot in **operating systems**, **Databases**, **Multithreading / parallel programs**, **Web servers**, **JavaScript with async operations**.

Race conditions are prevented using;
- 
- Locks
- Mutexes
- Semaphores
- Atomic operations
- Proprer async handling


    In JavaScript, operations are single-threaded, but async operations like; setTimeOut, fetch, and promises acnd still use race conditions when multple async tasks share the same variable and finish in an unpredictable order.


    # Callback Hell

    Callback hell happens when there are **callbacks inside callbacks inside callbacks**, making code hard read, debug and maintain.
     It is also called the pyramid of doom and each step depends on the previous one.

     Callback hell are by using callbacks for;
     - setTimeOut
     - AJAX / fetch
     - File reading
     - Chaining async tasks without structure

     Callback hell are avoided by;
     - Naming functions
     - Promises ( .then chaining)
     - Async / Await

     Async / await solves callback hell by flattening nested callbacks into readable, sequential code without changing asynchronous behavior. It is more like a pause, when this step is completed move to the next step, unlike callbacks that creates nested dependencies that make code hard to read.


