---
author: "volyx"
title:  "1570. Dot Product of Two Sparse Vectors"
date: "2021-11-18"
# description: "Sample article showcasing basic Markdown syntax and formatting for HTML elements."
tags:  ["leetcode", "medium", "fb", "array"]
categories: ["leetcode"]
# series: ["Themes Guide"]
# aliases: ["migrate-from-jekyl"]
# ShowToc: true
# TocOpen: true
# weight: 2
---

![1570. Dot Product of Two Sparse Vectors](https://leetcode.com/problems/dot-product-of-two-sparse-vectors/)

Given a stream of integers and a window size, calculate the moving average of all integers in the sliding window.

Implement the MovingAverage class:

- MovingAverage(int size) Initializes the object with the size of the window size.
- double next(int val) Returns the moving average of the last size values of the stream.

```txt
Example 1:

Input
["MovingAverage", "next", "next", "next", "next"]
[[3], [1], [10], [3], [5]]
Output
[null, 1.0, 5.5, 4.66667, 6.0]

Explanation
MovingAverage movingAverage = new MovingAverage(3);
movingAverage.next(1); // return 1.0 = 1 / 1
movingAverage.next(10); // return 5.5 = (1 + 10) / 2
movingAverage.next(3); // return 4.66667 = (1 + 10 + 3) / 3
movingAverage.next(5); // return 6.0 = (10 + 3 + 5) / 3
```

Constraints:

- 1 <= size <= 1000
- -10^5 <= val <= 10^5
- At most 104 calls will be made to next.

## Solution

```java
class MovingAverage {
    
    double sum = 0.0;
    Deque<Integer> deq;
    int n = 0;

    public MovingAverage(int size) {
        deq = new ArrayDeque<>(size);
        n = size;
    }
    
    public double next(int val) {
        sum += val;
        deq.push(val);
        
        if (deq.size() > n) {
            Integer prev = deq.pollLast();
            sum -= prev;
        }
        return sum / deq.size();
    }
}

/**
 * Your MovingAverage object will be instantiated and called as such:
 * MovingAverage obj = new MovingAverage(size);
 * double param_1 = obj.next(val);
 */
```
