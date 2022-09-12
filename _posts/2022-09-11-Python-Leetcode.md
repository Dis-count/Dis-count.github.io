---
layout: post
title: How to test Python in Leetcode
date: 2022-09-11
categories: Programming
tags: [Python]
---

## 实例化类(Manually)

After finishing your method, copy the input in the example, then have a test.

```python
class Solution:
    def gcdOfStrings(self, str1: str, str2: str) -> str:
        return ''


if __name__ == "__main__":
    s = Solution()
# 测试Example中的用例1
# Input: str1 = "ABCABC", str2 = "ABC"
# Output: "ABC"
    str1 = "ABCABC"
    str2 = "ABC"
    s.gcdOfStrings(str1, str2)
# or the other way
    assert s.isPalindrome(919) is True
    assert s.myAtoi('123 345 www 234') == 123
```

## Automatically

[reference](https://www.cnblogs.com/gradual/p/14111829.html)
