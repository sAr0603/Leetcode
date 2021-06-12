# [{{title}}]()

---

### Hints :

- Topics :
  - #
  - #
    - #
  - #
  - #

---

## Explanation :

- **Key observations**:

  - > # = `prefix[right] -prefix[left]``

  - > invariant = `subArraySum(left,right) >=k`

  - > dp = `we have to minimize left for all rights`

  - > observation-lemma = positions where `prefix[left]` has smaller value ...has higher chances of being in ans by looking at the invariant

  - > algorithm = we start looking at smallest value then go on to a bit larger value but at the benefit of optimization of length

  - > DS = MonoQueue  can do the above in **O(1)** time per operation

If we accumulate array A to obtain B, then `B[l] <= B[r] - K` indicates `sum(A[l:r]) >= K`. Given `B[r]`, the problem is equivalent to finding the **nearest** previous element `B[l]` such that `B[l] <= B[r] - K`.

We maintain a **increasing queue** here because, given a new `B[i]`, the larger element on the left are inferior than `B[i]` as a candidate to make some future element `B[j] >= B[i] + K` (`j > i`).

---

## Solution :

```python
code here
```
