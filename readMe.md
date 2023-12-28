### Suffix Array and Related Algorithms

This repository includes Python implementations of various algorithms related to suffix arrays. Suffix arrays are data structures that provide efficient solutions to numerous string-related problems, such as pattern matching, substring search, and more. The code in this repository covers algorithms for constructing suffix arrays, manipulating them, and performing searches on them.

### Algorithms Included:

1. **Naive Suffix Array Construction (naive):**
   - Constructs a suffix array using a naive approach.

2. **Karp-Miller-Rosenberg Suffix Array Construction (prefix_doubling):**
   - Constructs a suffix array using the Karp-Miller-Rosenberg algorithm.

3. **Kärkkäinen-Sanders Suffix Array Construction (skew):**
   - Constructs a suffix array using the Kärkkäinen-Sanders algorithm.

4. **Larsson-Sadakane Suffix Array Construction (larsson_sadakane):**
   - Constructs a suffix array using the Larsson-Sadakane algorithm.

5. **Nong-Zhang-Chan Suffix Array Construction (induced_sorting):**
   - Constructs a suffix array using the Nong-Zhang-Chan algorithm.

6. **Ko-Aluru Suffix Array Construction (small_large):**
   - Constructs a suffix array using the Ko-Aluru algorithm.

7. **Build Suffix Array from Suffix Tree (from_suffix_tree):**
   - Constructs a suffix array from a given suffix tree.

8. **Substring Containment (contains):**
   - Checks if the suffix array contains a given substring.

### Usage:

```python
from suffix_array_algorithms import (
    naive, prefix_doubling, skew, larsson_sadakane,
    induced_sorting, small_large, from_suffix_tree, contains
)

# Example usage
text = "banana"
n = len(text)

# Constructing suffix arrays
sa_naive = naive(text, n)
sa_kmr = prefix_doubling(text, n)
sa_ks = skew(text, n)
sa_ls = larsson_sadakane(text, n)
sa_nzc = induced_sorting(text, n)
sa_ka = small_large(text, n)

# Constructing suffix array from suffix tree
from suffix_tree_algorithms import build_suffix_tree
suffix_tree = build_suffix_tree(text)
sa_st = from_suffix_tree(suffix_tree, n)

# Searching for substrings
substring = "ana"
result_contains = list(contains(sa_naive, text, substring, n, len(substring)))
```

Choose the algorithm that best suits your requirements based on the characteristics of your input string.

### License:

This code is provided under the MIT License. Refer to the [LICENSE](LICENSE) file for more details.