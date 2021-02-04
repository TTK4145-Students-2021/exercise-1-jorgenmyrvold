# Results of running foo.go
The result of running foo varies emensly and is not deterministic. This is due to the two functions reading and writing to the same variable `i` simultaniously. When `incrementing()` runs it read `i`, increment it and writes it back to memory. If `decrementing()` reads `i` simultaniously this will cause a race condition and the output is corrupted.

To avoid this we can use waitgroups or mutexes, but i guess we'll come back to that in exercise 2.
