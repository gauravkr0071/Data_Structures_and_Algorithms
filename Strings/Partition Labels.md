### __Partition Labels__
[Problem Link](https://leetcode.com/problems/partition-labels/)

You are given a string s. We want to partition the string into as many parts as possible so that each letter appears in at most one part.
Return a list of integers representing the size of these parts.

 

__Example 1:__

Input: s = "ababcbacadefegdehijhklij" \
Output: [9,7,8] \
Explanation: \
The partition is "ababcbaca", "defegde", "hijhklij". \
This is a partition so that each letter appears in at most one part. \
A partition like "ababcbacadefegde", "hijhklij" is incorrect, because it splits s into less parts. \
__Example 2:__

Input: s = "eccbbbbdec" \
Output: [10] \
 Constraints: \
1 <= s.length <= 500 \
s consists of lowercase English letters.

```java
public List<Integer> partitionLabels(String S) {
        if(S == null || S.length() == 0){
            return null;
        }
        List<Integer> list = new ArrayList<>();
        int[] map = new int[26];  // record the last index of the each char

        for(int i = 0; i < S.length(); i++){
            map[S.charAt(i)-'a'] = i;
        }
        // record the end index of the current sub string
        int last = 0;
        int start = 0;
        for(int i = 0; i < S.length(); i++){
            last = Math.max(last, map[S.charAt(i)-'a']);
            if(last == i){
                list.add(last - start + 1);
                start = last + 1;
            }
        }
        return list;
    }
````
