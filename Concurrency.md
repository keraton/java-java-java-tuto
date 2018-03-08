# Java Concurrency

Knowing or not, it is possible that we are already using Java concurrency. 
The fact that we are using a servlet container (server), means indirectly we are using it.
Java Concurrency is a hard matter, but for most of the case we are only dealing with keeping the code tread safe.
Thread safe means that the code working correctly even if multiple threads access it concurrently.
Reaching Thread Safety can be done with working easily if we are not keeping any state.

This lesson will explain the basic of Java Concurrency and how to make our code Thread Safe.

# Thread & Runnable

* What is Thread ? 
* Since Java 1, we already use Thread class to create a Thread and to run it.
* But creation of Thread is expensive and resource consuming. 
* Instead of creating Thread, we should use Runnable interface.

# Excercice

* Create a multiple threads.
* Run it concurrently.

# Using Thread pool

* Instead creating thread, it is better to reuse it.
* This can be done by using thread pool.
* Use java Executors class.

# Exercice

* Create multiple thread using Executors and runnable

# How many thread ?

* Two types of execution : CPU consuming and IO consuming.
* For CPU consuming the number of parallel thread is limited by the processor core number.
* For IO : in theory is limitless.
* We can count the number of thread by using this formula : number of thread = ...(TBD)

# Dealing with mutable state

* In order to avoid data race in which one thread can corrupt state when other is reading on it we can use synchronize block.
* But synchronize means potential blocking thread (less perf) and can lead to a dead lock.

# Excercice

* Working with synchronize block.

# Use Concurrency framework

* Atomic
* Collection synchronize wrapper
* Collection concurrent.

# Summary

* Avoid working with mutable state.

