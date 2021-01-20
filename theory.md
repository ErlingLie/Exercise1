Exercise 1 - Theory questions
-----------------------------
 
 ### What is the difference between concurrency and parallelism?
 > Concurrency is when we run multiple computations in the same timeperiod. It does not mean that we run both tasks in the same time instant, as we can for instance switch quickly between the tasks (context switching). 

 > With parallellism on the other hand, the processes literally run simultaneously. This is possible if we for instance have a multi core CPU.
 
 ### Why have machines become increasingly multicore in the past decade?
 > Moore's law has flattened out, and we can no longer rely on processors getting exponentially faster.

 > Therefor, in order to continue increasing overall processing power manufacturers have started making multicore processors so that tasks can be run in parallell.
 
 ### Why do we divide software (programs) into concurrently executing parts (like threads or processes)?
 (Or phrased differently: What problems do concurrency help in solving?)
 > *Your answer here*
 
 ### Does creating concurrent programs make the programmer's life easier? Harder? Maybe both?
 (Come back to this after you have worked on part 4 of this exercise)
 > It can make the programmer's life harder, as it introduces new sources for bugs such as race conditions.
 
 ### What is the conceptual difference between threads and processes?
 > *Your answer here*
 
 ### Some languages support "fibers" (sometimes called "green threads") or "coroutines"? What are they?
 > *Your answer here*
 
 ### What is the Go-language's "goroutine"? A C/POSIX "pthread"?
 > *Your answer here*
 
 ### In Go, what does `func GOMAXPROCS(n int) int` change? 
 > GOMAXPROCS sets the maximum number of CPUs that can be executing simultaneously



 
 
 
 
