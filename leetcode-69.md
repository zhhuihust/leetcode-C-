#69. x 的平方根
	实现 int sqrt(int x) 函数。
	
	计算并返回 x 的平方根。
	
	x 保证是一个非负整数。

## Solution
	public class Solution {
    public int MySqrt(int x) {
        if(x==0)
            return 0;
        if(x==1)
            return 1;
        int left=0,right=x;
        while(left<right)
        {
            int mid = right-(right-left)/2;
            if(x/mid>=mid)
                left=mid;
            else
                right=mid-1;
        }
        return left;
    }
	