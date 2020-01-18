# Reasons for concurrency and parallelism


To complete this exercise you will have to use git. Create one or several commits that adds answers to the following questions and push it to a repository to complete the task. Remember to also submit your answers to Blackboard

When answering the questions, remember to use all the resources at your disposal. Asking the internet isn't a form of "cheating", it's a way of learning.

 ### What is concurrency? What is parallelism? What's the difference?
 > *When it comes to computing, concurrency is achieved by switching between different processes so rapidly that it gives the illusion of parallelism. Parallelism is when multiple processes are executed at the same time. 
 
 ### Why have machines become increasingly multicore in the past decade?
 > Traditionally increasing performance was done by increasing the clock frequency of the processor. This has a practical limit. A higher frequency allows for more operations to be performed each second. The problem with this approach is that in order to increase the clock frequency the voltage also has to increase and the power consumption is proportional to the square of the voltage. This leads to too much heat generation which limits the max frequency. To combat this multicore is used which allows for parallelism.
 
 ### What kinds of problems motivates the need for concurrent execution?
 (Or phrased differently: What problems do concurrency help in solving?)
 >  Increased program throughput—parallel execution of a concurrent program allows the number of tasks completed in a given time to increase proportionally to the number of processors according to Gustafson's law
 > High responsiveness for input/output—input/output-intensive programs mostly wait for input or output operations to complete. Concurrent programming allows the time that would be spent waiting to be used for another task.
 
 ### Does creating concurrent programs make the programmer's life easier? Harder? Maybe both?
 (Come back to this after you have worked on part 4 of this exercise)
 > Both.
 
 ### What are the differences between processes, threads, green threads, and coroutines?
 > Process:     A set of instructions executed sequentially.
 > Thread:      OS-managed, within the same address space as the parent and all its other threads. Possibly truly concurrent.
 > Green Thread: These are user-space projections of the same concept as threads, but are not OS-managed.
 > Coroutines:  Co-operatively multitasking threads, not truly concurrent. 
 
 ### Which one of these do `pthread_create()` (C/POSIX), `threading.Thread()` (Python), `go` (Go) create?
 > A new thread.
 
 ### How does pythons Global Interpreter Lock (GIL) influence the way a python Thread behaves?
 > The GIL synchronizes threads by only allowing one to be executed at a time.
 
 ### With this in mind: What is the workaround for the GIL (Hint: it's another module)?
 > Use another language.
 
 ### What does `func GOMAXPROCS(n int) int` change? 
 > The GOMAXPROCS variable limits the number of operating system threads that can execute user-level Go code simultaneously. There is no limit to the number of threads that can be blocked in system calls on behalf of Go code; those do not count against the GOMAXPROCS limit. 
