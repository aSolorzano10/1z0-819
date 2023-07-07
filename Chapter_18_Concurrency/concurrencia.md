# Concurrencia

## Interface Runnable

java.lang.Runnable is a functional interface that takes no arguments and returns no data.

```java
@FunctionalInterface public interface Runnable {
    void run();
}
```

## CREATING A THREAD

Java does not provide any guarantees about the order in which a thread will be processed once it is started.


## Creating Threads with the Concurrency API

### INTRODUCING THE SINGLE ‐ THREAD EXECUTOR

- The newSingleThreadExecutor() method to obtain an ExecutorService instance and the execute() method to perform asynchronous tasks.
- The method to create the service.
- With a single‐thread executor, results are guaranteed to be executed sequentially.


TABLE 18.1 ExecutorService methods

|Method name| Description                                         |
|-----------|-----------------------------------------------------|
|void execute(Runnable command)|Executes a Runnable task at some point in the future |
|Future<?> submit(Runnable task)|Executes a Runnable task at some point in the future and returns a Future representing the task|
|<T> Future<T> submit(Callable<T> task)|Executes a Callable task at some point in the future and returns a Future representing the pending results of the task|
|<T> List<Future<T>> invokeAll(Collection<? extends Callable<T>> tasks) throws InterruptedException|Executes the given tasks and waits for all tasks to complete. Returns a List of Future instances, in the same order th|
|<T> T invokeAny(Collection<? extends Callable<T>> tasks) throws InterruptedException, ExecutionException|Executes the given tasks and waits for at least one to complete. Returns a Future instance for a complete task and cancels any unfinished tasks|


## Introducing Callable

The call() method returns a value and can throw a checked exception.

```java
@FunctionalInterface public interface Callable<V> {
    V call() throws Exception;
}
```

The Callable interface is often preferable over Runnable

