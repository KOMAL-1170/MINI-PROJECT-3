#1
from itertools import combinations

# Define the set
S = {-12, -3, -6, 7, 2, -2, 6, 3, 9, -7, -5, -8, 1, 11, -9, -4}

# Set the desired subset size
subset_size = 5

# Find all combinations of the specified size whose sum is zero
zero_sum_subsets = [subset for subset in combinations(S, subset_size) if sum(subset) == 0]

# Print the results
for subset in zero_sum_subsets:
    print(subset)

# Optional: print total count
print(f"Total subsets found: {len(zero_sum_subsets)}")
#2
from itertools import combinations

# Given set
S = {-12, -3, -6, 7, 2, -2, 6, 3, 9, -7, -5, -8, 1, 11, -9, -4}

# Range of subset sizes
min_size = 3
max_size = 6

zero_sum_subsets = []

# Iterate over subset sizes from 3 to 6
for size in range(min_size, max_size + 1):
    # Check all combinations of that size
    for subset in combinations(S, size):
        if sum(subset) == 0:
            zero_sum_subsets.append(subset)

# Print all subsets found
for subset in zero_sum_subsets:
    print(subset)

print(f"Total subsets found: {len(zero_sum_subsets)}")
