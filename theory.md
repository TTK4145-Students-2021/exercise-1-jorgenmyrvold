Exercise 1 - Theory questions
-----------------------------
 
 ### What is the difference between concurrency and parallelism?
 > *Concurrency is when some processes are run alternating on one or more processors. It does not have to run exactly simoultaniously, but it can cause determinism problems. Parallellism is when processes actually run simoultaniously on different processors*
 
 ### Why have machines become increasingly multicore in the past decade?
 > *The technology have developed such that it allowes for more computational power in computers and also the use of multiple cores. In adition there has been a need for more efficient computations which has led to widespread use of parallelism which demads multiple cores to work efficiently*
 
 ### Why do we divide software (programs) into concurrently executing parts (like threads or processes)?
 (Or phrased differently: What problems do concurrency help in solving?)
 > *By executing different parts of SW in parallell we can have huge performance benefits. Cases where this kind of computation can benefit is for example in image processing where multiple operaitons has to be done on each pixel, and the operations don't depend on eachother's output. The performance benefits are also large in real-time systems where there are multiple processes going on at the same time. In this case concurrency might also cause problems, but as long as it is taken care of, there are large benefits here as well*
 
 ### Does creating concurrent programs make the programmer's life easier? Harder? Maybe both?
 (Come back to this after you have worked on part 4 of this exercise)
 > *Concurrent programs will in most case increase the complexity, and often cause some problems which can be harder to debug, but at the same time there is a tradeoff between efficiency and complexity. In some systems there are requirements to the system which only is possible to meet by using concurrent programs*
 
 ### What is the conceptual difference between threads and processes?
 > *Your answer here*
 
 ### Some languages support "fibers" (sometimes called "green threads") or "coroutines"? What are they?
 > *Your answer here*
 
 ### What is the Go-language's "goroutine"? A C/POSIX "pthread"?
 > *It is a way of implementing threads. It spawns at thread that start running in paralell to the main thread.*
 
 ### In Go, what does `func GOMAXPROCS(n int) int` change? 
 > *The number of processes that can be run simoultaniously. For cases when you want to have parallelism this is usualy set to the number of CPUs, but there might also be performance benefits to running more processes than cores available. This is in part thanks to Gos way of implementing goroutines.*



 
 
 
 
