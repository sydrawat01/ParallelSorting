# Parallel Sorting

Your task is to implement a parallel sorting algorithm such that each partition of the array is sorted in parallel.
You will consider two different schemes for deciding whether to sort in parallel.

1. A cutoff (defaults to, say, 1000) which you will update according to the first argument in the command line when running. It's your job to experiment and come up with a good value for this cutoff. If there are fewer elements to sort than the cutoff, then you should use the system sort instead. 
2. Recursion depth or the number of available threads. Using this determination, you might decide on an ideal number (_t_) of separate threads (stick to powers of 2) and arrange for that number of partitions to be parallelized (by preventing recursion after the depth of _lg t_ is reached). 
3. An appropriate combination of these.

There is a _Main_ class and the _ParallelSort_ class in the _parallel_ package of this repository.
The _Main_ class can be used as is but the _ParallelSort_ class needs to be implemented where you see "TODO..." [it turns out that these TODOs are already implemented].
Unless you have a good reason not to, you should just go along with the Java8-style future implementations provided for you in the class repository.

You must prepare a report that shows the results of your experiments and draws a conclusion (or more) about the efficacy of this method of parallelizing sort. Your experiments should involve sorting arrays of sufficient size for the parallel sort to make a difference. You should run with many different array sizes (they must be sufficiently large to make parallel sorting worthwhile, obviously) and different cutoff schemes.
For varying the number of threads available, you might want to consult the following resources:
- [https://www.callicoder.com/java-8-completablefuture-tutorial/#a-note-about-executor-and-thread-pool](https://www.callicoder.com/java-8-completablefuture-tutorial/#a-note-about-executor-and-thread-pool)
- [https://stackoverflow.com/questions/36569775/how-to-set-forkjoinpool-with-the-desired-number-of-worker-threads-in-completable](https://stackoverflow.com/questions/36569775/how-to-set-forkjoinpool-with-the-desired-number-of-worker-threads-in-completable)

Good luck and enjoy.