class Solution {
public:
    int minOperations(vector<int>& nums, int x) {
        // int n = nums.size();
        // int l = 0, r = n - 1;
        // int x1 = x, count1 = 0;

        // while(l <= r && x1 > 0)
        // {
        //     if(nums[l] <= x1)
        //     {
        //         x1 -= nums[l];
        //         l++;
        //         count1++;
        //     }
        //     else if(nums[r] <= x1)
        //     {
        //         x1 -= nums[r];
        //         r--;
        //         count1++;
        //     }
        //     else
        //         break;
        // }

        // if(x1 != 0) count1 = INT_MAX;

        // l = 0; r = n - 1;
        // int x2 = x, count2 = 0;

        // while(l <= r && x2 > 0)
        // {
        //     if(nums[r] <= x2)
        //     {
        //         x2 -= nums[r];
        //         r--;
        //         count2++;
        //     }
        //     else if(nums[l] <= x2)
        //     {
        //         x2 -= nums[l];
        //         l++;
        //         count2++;
        //     }
        //     else
        //         break;
        // }

        // if(x2 != 0) count2 = INT_MAX;

        // int ans = min(count1, count2);

        // if(ans == INT_MAX)
        //     return -1;

        // return ans;

        int n=nums.size();
        int total=0;
        for(int i=0; i<n; i++)
        {
            total+=nums[i];
        }
        int target=total-x;
        if(target<0) {return -1;}
        
        int l=0; 
        int sum=0;
        int maxLen=-1;

        for(int r=0; r<n; r++)
        {
            sum+=nums[r];
            while(sum>target)
            {
                sum-=nums[l];
                l++;
            }
            if(sum==target)
            {
                maxLen = max(maxLen, r-l+1);
            }

        }
        if(maxLen == -1)
            return -1;

        return n - maxLen;
    }
};
