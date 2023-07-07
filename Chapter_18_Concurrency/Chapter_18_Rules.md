# Rules

### Defining the task that a Thread instance will execute can be done two ways in Java:

- Provide a Runnable object or lambda expression to the Thread constructor.
- Create a class that extends Thread and overrides the run() method.


### Reviewing the Lock Framework
To review, the *ReentrantLock* class supports the same features as a *synchronized* block, while adding a number of improvements.

- Ability to request a lock without blocking
- Ability to request a lock while blocking for a specified amount of time
- A lock can be created with a fairness property, in which the lock is granted to threads in the order it was requested.