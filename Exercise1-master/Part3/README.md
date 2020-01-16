# Reasons for concurrency and parallelism


To complete this exercise you will have to use git. Create one or several commits that adds answers to the following questions and push it to your groups repository to complete the task.

When answering the questions, remember to use all the resources at your disposal. Asking the internet isn't a form of "cheating", it's a way of learning.

 ### What is concurrency? What is parallelism? What's the difference?
 > *Concurrency means multiple computations are happening at the same time but in no specific order. They dont really run at the same time, but
when the first task is in waiting state, CPU is assigned to second task to complete it’s part of task.

Parallelism is performing several computations at the same time, making programs faster by literally doing two or more things at the same time. To use parallelism one requires hardware with multiple processing units so that each unit can handle one task each.

The difference is concurrency does tasks almost simultaniously while parallelism is performing several tasks actually at the same time.*


 ### Why have machines become increasingly multicore in the past decade?
 > *Because a multicore processor can run instructions on separate cores at the same time. This makes us able to increase run speed of programs by parallelism instead of needing faster processors which becomes harder and harder as the processors get faster.*

 ### What kinds of problems motivates the need for concurrent execution?
 (Or phrased differently: What problems do concurrency help in solving?)
 > *Concurrency can make problems with minimum two tasks or more compute faster. In these cases the CPU can work concurrently on multiple tasks, resulting in less waiting time and making the program run faster. Almost all modern day problems include several tasks, meaning concurrency is important to reduce runtime in almost all cases.*

 ### Does creating concurrent programs make the programmer's life easier? Harder? Maybe both?
 (Come back to this after you have worked on part 4 of this exercise)
 > **

 ### What are the differences between processes, threads, green threads, and coroutines?
 > *A process is an instance of a running program that is isolated from the other processes on the same machine. A process has it's own private section of the machine's memory. A thread is the unit of execution within a process. A process can have one or many threads. Green threads are threads that are scheduled by a virtual machine instead of natively by the underlying OS. Coroutines are a generalization of subroutines. Coroutines are used for cooperative multitasking where a process give away control periodically to enable multiple applications to be run simultaneously.*

 ### Which one of these do `pthread_create()` (C/POSIX), `threading.Thread()` (Python), `go` (Go) create?
 > *`pthread_create()` - Thread
    `threading.Thread()`- Thread
    `go` - Process*

 ### How does pythons Global Interpreter Lock (GIL) influence the way a python Thread behaves?
 > *GIL is a lock that allows only one thread to hold the control of the Python interpreter. This  makes any CPU-bound Python program single-threaded, making it only able to run one thread at a time. This was made to ensure multiple threads can't write to the same location in the memory heap.*

 ### With this in mind: What is the workaround for the GIL (Hint: it's another module)?
 > *Use multiprocessing.*

 ### What does `func GOMAXPROCS(n int) int` change?
 > *Sets the maximum number of CPUs that can be executing simultaneously and returns the previous setting.*
