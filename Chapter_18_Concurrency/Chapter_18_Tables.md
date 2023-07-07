# Tables

### TABLE 18.1 ExecutorService methods

| Method name                                                                                              | Description                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| void execute(Runnable command)                                                                           | Executes a *Runnable* task at some point in the future                                                                                            |
| Future<?> submit(Runnable task)                                                                          | Executes a *Runnable* task at some point in the future and returns a *Future* representing the task                                               |
| <T> Future<T> submit(Callable<T> task)                                                                   | Executes a *Callable* task at some point in the future and returns a *Future* representing the pending results of the task                        |
| <T> List<Future<T>> invokeAll(Collection<? extends Callable<T>> tasks) throws InterruptedException       | Executes the given tasks and waits for all tasks to complete. Returns a *List* of *Future* instances, in the same order th                        |
| <T> T invokeAny(Collection<? extends Callable<T>> tasks) throws InterruptedException, ExecutionException | Executes the given tasks and waits for at least one to complete. Returns a *Future* instance for a complete task and cancels any unfinished tasks |


### TABLE 18.2 Future methods
| Method name                                   | Description                                                                                                                                                                       |
|-----------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| boolean isDone()                              | Returns *true* if the task was completed, threw an exception, or was cancelled                                                                                                    |
| boolean isCancelled()                         | Returns *true* if the task was cancelled before it completed normally                                                                                                             | 
| boolean cancel(boolean mayInterruptIfRunning) | Attempts to cancel execution of the task and returns *true* if it was successfully cancelled or *false* if it could not be cancelled or is complete                               |
| V get()                                       | Retrieves the result of a task, waiting endlessly if it is not yet available                                                                                                      | 
| V get(long timeout, TimeUnit unit)            | Retrieves the result of a task, waiting the specified amount of time. If the result is not ready by the time the timeout is reached, a checked *TimeoutException* will be thrown. |



### TABLE 18.3 TimeUnit values
| Enum name             | Description                                         |
|-----------------------|-----------------------------------------------------|
| TimeUnit.NANOSECONDS  | Time in one‐billionth of a second (1/1,000,000,000) |
| TimeUnit.MICROSECONDS | Time in one‐millionth of a second (1/1,000,000)     |
| TimeUnit.MILLISECONDS | Time in one‐thousandth of a second (1/1,000)        |
| TimeUnit.SECONDS      | Time in seconds                                     |
| TimeUnit.MINUTES      | Time in minutes                                     | 
| TimeUnit.HOURS        | Time in hours                                       | 
| TimeUnit.DAYS         | Time in days                                        |


### TABLE 18.4 ScheduledExecutorService methods
| Method Name                                                                            | Description                                                                                                                                                                          |
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| schedule(Callable<V> callable, long delay, TimeUnit unit)                              | Creates and executes a *Callable* task after the given delay                                                                                                                         | 
| schedule(Runnable command, long delay, TimeUnit unit)                                  | Creates and executes a *Runnable* task after the given delay                                                                                                                         | 
| scheduleAtFixedRate(Runnable command, long initialDelay, long period, TimeUnit unit)   | Creates and executes a *Runnable* task after the given initial delay, creating a new task every period value that passes                                                             | 
| scheduleWithFixedDelay(Runnable command, long initialDelay, long delay, TimeUnit unit) | Creates and executes a *Runnable* task after the given initial delay and subsequently with the given delay between the termination of one execution and the commencement of the next |


### TABLE 18.5 Executors factory methods
| Method                                                      | Description                                                                                                                                                                        |
|-------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ExecutorService newSingleThreadExecutor()                   | Creates a single‐threaded executor that uses a single worker thread operating off an unbounded queue. Results are processed sequentially in the order in which they are submitted. |
| ScheduledExecutorService newSingleThreadScheduledExecutor() | Creates a single‐threaded executor that can schedule commands to run after a given delay or to execute periodically                                                                |
| ExecutorServicenewCachedThreadPool()                        | Creates a thread pool that creates new threads as needed but will reuse previously constructed threads when they are available                                                     |
| ExecutorServicenewFixedThreadPool(int)                      | Creates a thread pool that reuses a fixed number of threads operating off a shared unbounded queue                                                                                 |
| ScheduledExecutorServicenewScheduledThreadPool(int)         | Creates a thread pool that can schedule commands to run after a given delay or to execute periodically                                                                             |


### TABLE 18.6 Atomic classes
| Class Name    | Description                                    |
|---------------|------------------------------------------------|
| AtomicBoolean | A boolean value that may be updated atomically |
| AtomicInteger | An int value that may be updated atomically    |
| AtomicLong    | A long value that may be updated atomically    |


### TABLE 18.7 Common atomic methods
| Method name       | Description                                                                  |
|-------------------|------------------------------------------------------------------------------|
| get()             | Retrieves the current value                                                  |
| set()             | Sets the given value, equivalent to the assignment = operator                |
| getAndSet()       | Atomically sets the new value and returns the old value                      |
| incrementAndGet() | For numeric classes, atomic pre‐increment operation equivalent to *++value*  |
| getAndIncrement() | For numeric classes, atomic post‐increment operation equivalent to *value++* | 
| decrementAndGet() | For numeric classes, atomic pre‐decrement operation equivalent to *‐‐value*  |
| getAndDecrement() | For numeric classes, atomic post‐decrement operation equivalent to *value‐‐* |


### TABLE 18.8 Lock methods
| Method                         | Description                                                                                                                                         |
|--------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| void lock()                    | Requests a lock and blocks until lock is acquired                                                                                                   |
| void unlock()                  | Releases a lock                                                                                                                                     |
| boolean tryLock()              | Requests a lock and returns immediately. Returns a boolean indicating whether the lock was successfully acquired                                    |
| boolean tryLock(long,TimeUnit) | Requests a lock and blocks up to the specified time until lock is required. Returns a boolean indicating whether the lock was successfully acquired |


### TABLE 18.9 Concurrent collection classes
| Class name            | Java Collections Framework interfaces          | Elements ordered? | Sorted? | Blocking? |
|-----------------------|------------------------------------------------|-------------------|---------|-----------|
| ConcurrentHashMap     | ConcurrentMap                                  | No                | No      | No        |
| ConcurrentLinkedQueue | Queue                                          | Yes               | No      | No        |
| ConcurrentSkipListMap | ConcurrentMap </br>SortedMap </br>NavigableMap | Yes               | Yes     | No        |
| ConcurrentSkipListSet | SortedSet </br>NavigableSet                    | Yes               | Yes     | No        |
| CopyOnWriteArrayList  | List                                           | No                | No      | No        |
| LinkedBlockingQueue   | BlockingQueue                                  | Yes               | No      | Yes       |


### TABLE 18.10 BlockingQueue waiting methods
| Method  name                            | Description                                                                                                                                    |
|-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| offer(E e, long timeout, TimeUnit unit) | Adds an item to the queue, waiting the specified time and returning *false* if the time elapses before space is available                      |
| poll(long timeout, TimeUnit unit)       | Retrieves and removes an item from the queue, waiting the specified time and returning *null* if the time elapses before the item is available |


### TABLE 18.11 Synchronized collections methods

synchronizedCollection(Collection<T> c) 
synchronizedList(List<T> list)
synchronizedMap(Map<K,V> m)
synchronizedNavigableMap(NavigableMap<K,V> m)
synchronizedNavigableSet(NavigableSet<T> s)
synchronizedSet(Set<T> s)
synchronizedSortedMap(SortedMap<K,V> m)
synchronizedSortedSet(SortedSet<T> s)