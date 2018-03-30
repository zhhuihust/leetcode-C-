# 28. 实现strStr()


Implement strStr().

Return the index of the first occurrence of needle in haystack, or -1 if needle is not part of haystack.

###Example 1:

	Input: haystack = "hello", needle = "ll"
	Output: 2
###	Example 2:

	Input: haystack = "aaaaa", needle = "bba"
	Output: -1
# Answer
	public class Solution {
	    public int StrStr(string haystack, string needle) {
	        for(int i=0;;i++)
	        {
	            for(int j=0;;j++)
	            {
	                if(j==needle.Length) return i;
	                if(i+j==haystack.Length) return -1;
	                if(needle[j]!=haystack[i+j]) break;
	            }
	                
	        }
	            
	    }
	}