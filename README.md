# Sorting Algorithm Experiments

An educational Python comparison of **insertion sort** and **merge sort**,
with timing experiments on shuffled, sorted, and reverse-sorted integer arrays.

## What is included

| File | Purpose |
| --- | --- |
| [Sort.py](Sort.py) | In-place insertion sort and recursive merge sort |
| [TestInsertion.py](TestInsertion.py) | Insertion-sort experiments for three input orders |
| [TestMergeSort.py](TestMergeSort.py) | Merge-sort experiments for shuffled and ordered input |
| [main.py](main.py) | Runs all five plotting experiments |

## Getting started

Use **Python 2.7** with a compatible Matplotlib installation in an isolated
legacy environment. The benchmark scripts mutate the results of `range()`,
which are lists in Python 2 but not in Python 3. Python 2 is end-of-life.

From the repository root:

```sh
python2 main.py
```

Each experiment displays a plot. Close the current plot window to move on to
the next experiment.

## Using the algorithms

```python
from Sort import Insertion_sort, Merge_sort

values = [5, 2, 4, 1, 3]
Insertion_sort(values)

other_values = [9, 7, 8, 6]
Merge_sort(other_values, 0, len(other_values) - 1)
```

Both functions mutate the supplied list. Merge sort takes inclusive start and
end indices.

## Interpreting the results

The project illustrates input-order sensitivity and the distinction between
quadratic insertion-sort behavior and divide-and-conquer sorting. The scripts
are historical experiments, not a rigorous benchmark harness: repetitions reuse
the same list reference, so later repetitions can receive already-sorted input.
Consider that limitation before drawing performance conclusions.

## Project provenance

This repository is a fork of
[edoardore/Sorting-Algorithm](https://github.com/edoardore/Sorting-Algorithm).
The original implementation and history are preserved.
