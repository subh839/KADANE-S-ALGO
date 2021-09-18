# KADANE-S-ALGO

int maxSubArray(vector<int>& nums) {
        
        int currentSum = 0, totalSum = INT_MIN;
        
        for(int i=0; i<nums.size(); i++) {
            
            //Sum till this point ======= Current Sum till this point + this element
            currentSum = currentSum + nums[i]; 
            
            //If the current maximum array sum is greater than the global total. Update it
            totalSum = max(totalSum, currentSum);
            
            //If you get current as less thn 0 then its no point in carrying forward. Make it 0
            currentSum = max(0,currentSum);
    }
        return totalSum;
    }
