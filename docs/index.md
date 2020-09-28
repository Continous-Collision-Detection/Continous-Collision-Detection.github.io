# A Large Scale Benchmark and an Inclusion-Based Algorithm for Continuous Collision Detection

## Paper

Coming soon!

## Abstract

We introduce a large scale benchmark for continuous collision detection (CCD) algorithms, composed of queries manually constructed to highlight challenging degenerate cases and automatically generated using existing simulators to cover common cases. We use the benchmark to evaluate the accuracy, correctness, and efficiency of state-of-the-art continuous collision detection algorithms, both with and without minimal separation.

We discover that, despite the widespread use of CCD algorithms, existing algorithms are either: (1) correct but impractically slow, (2) efficient but incorrect, introducing false negatives which will lead to interpenetration, or (3) correct but over conservative, reporting a large number of false positives which might lead to inaccuracies when integrated in a simulator.

By combining the seminal interval root finding algorithm introduced by Snyder in 1992 with modern predicate design techniques, we propose a simple and efficient CCD algorithm. This algorithm is competitive with state of the art methods in terms of runtime while conservatively reporting the time of impact and allowing explicit trade off between runtime efficiency and number of false positives reported.

## Source Code and Data

* [GitHub Organization](https://github.com/Continuous-Collision-Detection)
* [Wrapper and Benchmark](https://github.com/Continuous-Collision-Detection/CCD-Wrapper)
* [Novel Inclusion-Based CCD](https://github.com/Continuous-Collision-Detection/Tight-Inclusion)
* Queries:
    * [Sample](https://github.com/Continuous-Collision-Detection/Sample-Queries)
    * Full Dataset (coming soon)
