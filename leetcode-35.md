#35. 搜索插入位置
给定一个排序数组和一个目标值，如果在数组中找到目标值则返回索引。如果没有，返回到它将会被按顺序插入的位置。

你可以假设在数组中无重复元素。

 

###案例 1:

	输入: [1,3,5,6], 5
	输出: 2
 

###案例 2:

	输入: [1,3,5,6], 2
	输出: 1
	 

###案例 3:
	
	输入: [1,3,5,6], 7
	输出: 4

#Answer
	public class Solution {
	    public int SearchInsert(int[] nums, int target) {
	        int low = 0, high = nums.Length-1;
	        while(low<=high){
	            int mid = (low+high)/2;
	            if(nums[mid] == target) return mid;
	            else if(nums[mid] > target) high = mid-1;
	            else low = mid+1;
	        }
	        return low;
	    }
	}