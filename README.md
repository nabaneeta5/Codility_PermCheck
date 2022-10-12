# Codility_PermCheck
Check whether array A is a permutation.

# Task description
A non-empty array A consisting of N integers is given.

A permutation is a sequence containing each element from 1 to N once, and only once.

# Link Details
[training8XRCQD-TPE](https://app.codility.com/demo/results/training8XRCQD-TPE/)

# Programming Language
Java SE 11

# Solution Code

```
import java.util.*;
import java.util.stream.Collectors;


class Solution {
    public int solution(int[] A) {
        // write your code in Java SE 11
        int[] B=Arrays.stream(A).distinct().toArray();
        if(A.length!=B.length){
            return 0;
        }
        else{
            int[] C=Arrays.stream(A).sorted().toArray();
            int count=C[C.length-1];

            while(count>0){
                if(Arrays.binarySearch(C,count)<0){
                    return 0;
                }
                count--;
            }
            return 1;
        }
           
    }
}

```


