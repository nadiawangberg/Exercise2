# Mutex and Channel basics

### What is an atomic operation?
> Atomic operations are operations that run completely independent of another processes. An atomic load reads the entire value as it appeared at a single moment of time. Different threads can manipulate a shared variable at the same time, if they both use atomic operations. An advantage of atomic operations is that they are relatively quick compared to locks, the other threads see it as happening instantaneously (do not suffer from deadlock and convoying).

### What is a semaphore?
> Like mutex lock it is used to protect the critical section and avoid race conditions. It restricts the amount of users (threads) that can access a common shared resource at the same time. When a new thread accesses the resource the semaphore is decremented, when it is done it is incremented. When the semahore is 0 a new thread cannot acces the resource. No ownership. 

### What is a mutex?
> In a multithreaded application two threads might have a shared variable (common resource) on shared memory. The shared resource can often not be accessed at the same time, as errors might occur (such as in task1). Mutex (mutual exclusion) is a concept that ensures that only one thread is allowed to read/write to a variable at a time. 

### What is the difference between a mutex and a binary semaphore?
> A mutex lock and a binary semaphore are similar in the sence that they only allow one thread accessing the resource at a time. With a Semaphores there is no ownership, the "semaphore" owns the shared resource like a gatekeeper. With mutex each thread has ownership over the resource when it can access it. A mutex can be released (unlocking the resource) only by the thread that had aquired it. A binary semaphore can be signaled by any thread (or process).

### What is a critical section?
> If two threads access a shared variable at the same time unexpteced erroneous behaviour might occur. The shared resource needs to be protected so it avoids concurrent access. The protected section is the critical, section a mutex could be used to protect this area. 

### What is the difference between race conditions and data races?
 > *Your answer here*

### List some advantages of using message passing over lock-based synchronization primitives.
> *Your answer here*

### List some advantages of using lock-based synchronization primitives over message passing.
> *Your answer here*
