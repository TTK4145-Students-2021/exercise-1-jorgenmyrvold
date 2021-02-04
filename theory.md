Exercise 1 - Theory questions
-----------------------------
 
 ### What is the difference between concurrency and parallelism?
 > *Concurrency is when some processes are run alternating on one or more processors. It does not have to run exactly simoultaniously, but it can cause determinism problems. Parallellism is when processes actually run simoultaniously on different processors*
 
 ### Why have machines become increasingly multicore in the past decade?
 > *The technology have developed such that it allowes for more computational power in computers and also the use of multiple cores. In addition there has been a need for more computational power which has led to widespread use of parallelism which demads multiple cores to work efficiently*
 
 ### Why do we divide software (programs) into concurrently executing parts (like threads or processes)?
 (Or phrased differently: What problems do concurrency help in solving?)
 > *If you want to do two or more tasks simoultaniously there can be large performance benefits by computing concrurrently. Writing concurrent programs can also improve the readability of your code*
 
 ### Does creating concurrent programs make the programmer's life easier? Harder? Maybe both?
 (Come back to this after you have worked on part 4 of this exercise)
 > *Concurrent programs will in most case increase the complexity, and often cause some problems which can be harder to debug, but at the same time there is a tradeoff between efficiency and complexity. In some systems there are requirements to the system which only is possible to meet by using concurrent programs*
 
 ### What is the conceptual difference between threads and processes?
 > *They are both features for executing code in parallell, but a general rule for differentiating is that threads (spawned from the same process) share the same memory space, but processes do not. A process is usually run by spawning a "main" thread to execute the code, and then any thread can spawn new threads.*
 
 ### Some languages support "fibers" (sometimes called "green threads") or "coroutines"? What are they?
 > *Fibers are much the same as a thread that supports multitasking, but contrary to threads which use preemptive multitasking, fibes use cooperative multitasking. While threads gets deligated some computation time by a scheduler, fibers yield controll on a periodic basis or when they are blocked. This means that fibers cooperate with eachother which is quite the opposite of threads that don't care about other threads in the same maner*
 
 ### What is the Go-language's "goroutine"? A C/POSIX "pthread"?
 > *Goroutines and pthreads are Go's and C's way of implementing threads. It spawns at thread that start running in paralell to the main thread.*
 
 ### In Go, what does `func GOMAXPROCS(n int) int` change? 
 > *The number of processes that can be run simoultaniously. For cases when you want to have parallelism this is usualy set to the number of CPUs, but there might also be performance benefits to running more processes than cores available. This is in part thanks to Gos way of implementing goroutines.*
