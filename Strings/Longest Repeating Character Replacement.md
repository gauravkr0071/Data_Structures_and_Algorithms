### __Longest Repeating Character Replacement__ : FOUND IT TOUGH
[Problem link]()

You are given a string s and an integer k. You can choose any character of the string and change it to\
any other uppercase English character. You can perform this operation at most k times.

Return the length of the longest substring containing the same letter you can get after performing the above operations.

 

__Example 1:__

Input: s = "ABAB", k = 2 \
Output: 4 \
Explanation: Replace the two 'A's with two 'B's or vice versa. \
__Example 2:__

Input: s = "AABABBA", k = 1 \
Output: 4 \
Explanation: Replace the one 'A' in the middle with 'B' and form "AABBBBA". \
The substring "BBBB" has the longest repeating letters, which is 4.
 

__Constraints:__ 

1 <= s.length <= 105 \
s consists of only uppercase English letters. \
0 <= k <= s.length


```java
public int characterReplacement(String s, int k) {
        int len = s.length();
        int[] count = new int[26];
        int start = 0, maxCount = 0, maxLength = 0;
        for (int end = 0; end < len; end++) {
            maxCount = Math.max(maxCount, ++count[s.charAt(end) - 'A']);
            while (end - start + 1 - maxCount > k) {
                count[s.charAt(start) - 'A']--;
                start++;
            }
            maxLength = Math.max(maxLength, end - start + 1);
        }
        return maxLength;
    }
```
