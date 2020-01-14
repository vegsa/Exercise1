# Reasons for concurrency and parallelism


To complete this exercise you will have to use git. Create one or several commits that adds answers to the following questions and push it to your groups repository to complete the task.

When answering the questions, remember to use all the resources at your disposal. Asking the internet isn't a form of "cheating", it's a way of learning.

 ### What is concurrency? What is parallelism? What's the difference?
 > Concurrency is that computer does two tasks at one time by switching between the two tasks. To the user it seems that the tasks runs in parallel, but the computer changes between multiple tasks, by setting the ones it is not working with in a wating state. Parallelism is that two tasks is runned at once by running them in parallell. For example, concurrency is that a person does two assignments at once by first doing a bit of the first, then a bit of the other and alters between them, while parallelism is that you have two persons, where one of them does the first and the other does the second one.
 
 ### Why have machines become increasingly multicore in the past decade?
 > That is because this improves the performance such that one can run multiple processes at the same time. Since the computer can do multiple things at once, the system speeds up. In addition, with a bigger core instead of multiple cores, it requires more power and you get more heat loss for example. 
 
 ### What kinds of problems motivates the need for concurrent execution?
 (Or phrased differently: What problems do concurrency help in solving?)
 > Concurrency help in solving problems involving lost updates, uncommitted data and inconsistent retrievals. This is problems that can arise because of the simultaneous execution of transactions over a shared database.
 
 ### Does creating concurrent programs make the programmer's life easier? Harder? Maybe both?
 (Come back to this after you have worked on part 4 of this exercise)
 > It can make the programmer's life both harder and easier. It depends on what the problem is. In Part 4 of this exercise it makes the life harder if we are going to find i, since we will get different i's from time to time. But if we had used two different variables for the two threads, it could have made the lifte easier.
 
 ### What are the differences between processes, threads, green threads, and coroutines?
 > A process is a part of a computer program that is executed by one or multiple threads. In a process we have program code and its activity. A thread can be seen as a module of a system or a process. Threads can share the resources, e.g. memory, while the processes are completely independent of each other. Green threads are threads which are scheduled by a virtual machine, while threads are scheduled by the underlying operative system. Coroutines are threads that are concurrent and not parallel.
 
 ### Which one of these do `pthread_create()` (C/POSIX), `threading.Thread()` (Python), `go` (Go) create?
 > pthread_create() creates a thread, threading.Thread() creates a green thread and go creates coroutines.
 
 ### How does pythons Global Interpreter Lock (GIL) influence the way a python Thread behaves?
 > Global Interpreter Lock prevents execution of multiple threads at once. This works such that when a thread wants to run, it has to wait for the GIL to be released by the other tread which is using it, if there is a thread that is using it. Only one thread can run at once within the interpreter. Then Python will work as it is single threaded. 

 ### With this in mind: What is the workaround for the GIL (Hint: it's another module)?
 > We can use the threading module.
 
 ### What does `func GOMAXPROCS(n int) int` change? 
 > The function changes the max number of CPUs that can execute Go code simultaneously.

