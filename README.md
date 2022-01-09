# MeshReconstruction-Parallelism

In part 1, I have modified MeshReconstruction.cpp file to achieve parallelism. I have used “#pragme omp parallel for” clause to parallelize for loops. I have stated the shared and private variables between loops. Also, I have stated that IntersectInfo and Triangulate should not be parallelize, each thread should wait for another to finish executing this section to enter this critical section.

In part 2, I have modified main.cpp file to achieve parallelism. I have used “#pragme omp parallel for” clause to parallelize for loops. I have stated the private variable “frame” between loops. Since I could not parallelize the updated value of twist for each loop, I have taken twist variable out of the loop and in another loop, I have added twist values for each loop to an array called “twistePerFrame”. I called this array’s needed index in the Mesh construction.
