	# 70. 爬楼梯

你正在爬楼梯。需要 n 步你才能到达顶部。

每次你可以爬 1 或 2 个台阶。你有多少种不同的方式可以爬到楼顶呢？

注意：给定 n 将是一个正整数。

 

#示例 1：

	输入： 2
	输出： 2
	说明： 有两种方法可以爬到顶端。
	
	1.  1 步 + 1 步
	2.  2 步
 

#示例 2：

	输入： 3
	输出： 3
	说明： 有三种方法可以爬到顶端。
	
	1.  1 步 + 1 步 + 1 步
	2.  1 步 + 2 步
	3.  2 步 + 1 步
#Solution
	public class Solution {
    public int ClimbStairs(int n) {
           int answer =1;
        for(int i=0,pre=0;i<n;i++) pre=(answer+=pre)-pre;
        return answer;
    }
	}

# 分析
本次的步数等于上次+上次-1次的结果