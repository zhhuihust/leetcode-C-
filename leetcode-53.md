#53. 最大子序和

给定一个序列（至少含有 1 个数），从该序列中寻找一个连续的子序列，使得子序列的和最大。

	例如，给定序列 [-2,1,-3,4,-1,2,1,-5,4]，
	连续子序列 [4,-1,2,1] 的和最大，为 6。
#分析

动态规划问题


#Answer
	public class Solution {
	    public int MaxSubArray(int[] nums) {
	         int n = nums.Length;
	        int[] dp = new int[n];
	        dp[0]=nums[0];
	        int max = dp[0];
	        
	        for(int i= 1;i<n;i++){
	            dp[i]=nums[i]+(dp[i-1]>0?dp[i-1]:0);
	            max = Math.Max(max,dp[i]);
	        }
	        
	        return max;
	    }
	}