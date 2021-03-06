#### Please add your answers to the ***Analysis of  Algorithms*** exercises here.

## Exercise I

a) O(log n)


b) O(n^2)


c) O(n)

## Exercise II

```python
import math
OPTIMAL_FLOOR = 8


def optimal_breaking_floor(top_floor):
    return optimal_floor(top_floor, 0)


def optimal_floor(upper_bound, lower_bound):

    if upper_bound == lower_bound:
        return upper_bound

    half_upper_lower = math.ceil((upper_bound - lower_bound) / 2)
    if is_egg_broken(upper_bound - half_upper_lower):
        upper_bound = upper_bound - half_upper_lower
    else:
        lower_bound = lower_bound + half_upper_lower

    return optimal_floor(upper_bound, lower_bound)


def is_egg_broken(floor):
    return True if floor >= OPTIMAL_FLOOR else False


print(optimal_breaking_floor(10))

```