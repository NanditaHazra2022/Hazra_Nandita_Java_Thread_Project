# Hazra_Nandita_Java_Thread_Project
This is a repository of Java programs on Thread execution control.

What is a thread?
Threads exist within a process — every process has at least one. Threads share the process's resources, including memory and open files. 
Multithreaded execution is an essential feature of the Java platform. Every application has at least one thread — or several, if you count "system" threads that do things like memory management and signal handling. But from the application programmer's point of view, you start with just one thread, called the main thread. This thread has the ability to create additional threads.

How thread gets executed?
Each thread is associated with an instance of the class Thread. 
A thread is a sequence of execution in a program. The Java Virtual Machine allows an application to have multiple threads of execution running concurrently.
Every thread has a priority. Threads with higher priority are executed in preference to threads with lower priority. Each thread may or may not also be marked as a daemon. When code running in some thread creates a new Thread object, the new thread has its priority initially set equal to the priority of the creating thread, and is a daemon thread if and only if the creating thread is a daemon.
When a Java Virtual Machine starts up, there is usually a single non-daemon thread (which typically calls the method named main of some designated class). The Java Virtual Machine continues to execute threads until either of the following occurs:
-	The exit method of class Runtime has been called and the security manager has permitted the exit operation to take place.
-	All threads that are not daemon threads have died, either by returning from the call to the run method or by throwing an exception that propagates beyond the run method.
There are two ways to create a new thread of execution. One is to declare a class to be a subclass of Thread. This subclass should override the run method of class Thread. An instance of the subclass can then be allocated and started. The other way to create a thread is to declare a class that implements the Runnable interface. That class then implements the run method. An instance of the class can then be allocated, passed as an argument when creating Thread, and started. 

How execution of thread is paused?
Thread.sleep causes the current thread to suspend execution for a specified period. This is an efficient means of making processor time available to the other threads of an application or other applications that might be running on a computer system. The sleep method can also be used for pacing.

What is an interrupt?
An interrupt is an indication to a thread that it should stop what it is doing and do something else. A thread sends an interrupt by invoking interrupt on the Thread object for the thread to be interrupted. For the interrupt mechanism to work correctly, the interrupted thread must support its own interruption. If the thread is frequently invoking methods that throw InterruptedException, it simply returns from the run method after it catches that exception.

How does one thread wait for completion of other?
Thread.join causes the current thread to pause execution until previous thread terminates.
