class Solution {
    public int maxSubArray(int[] nums) {
        int MaxSum=Integer.MIN_VALUE;//
        int Curr_sum=0;
        for(int i=0;i< nums.length;i++)
        {
            Curr_sum+=nums[i];//0+(-2)=-2//9
            if(Curr_sum>MaxSum)//5>-1//9>5
            {
                MaxSum=Curr_sum;//9
            }
            if(Curr_sum<0)
            {
                Curr_sum=0;
            }
        }
        return MaxSum;
    }
}
