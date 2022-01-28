# data-structure-and-algorithm
my data structure and algorithms questions solutions
Q.1:- Given an array of integers nums and an integer target, return indices of the two numbers such that they add up to target.

You may assume that each input would have exactly one solution, and you may not use the same element twice.

You can return the answer in any order.

 

Example 1:

Input: nums = [2,7,11,15], target = 9
Output: [0,1]
Explanation: Because nums[0] + nums[1] == 9, we return [0, 1]


    -:Algorithm:-
> Start
> Declare a vector result to return the result
> Declare the map to store the indexes
> repeat 5th step
> check one condition to check the sum and store the index in the map if the condition is true return it else store the indexes in the map
> End


      -:code:- "USING HASHMAP TECHNIQUE"
 vector<int> twoSum(vector<int>& nums, int target) {
        vector<int> result;
        map<int,int> m;
        for(int i=0;i<nums.size();i++)
        {
            int ntof=target-nums[i];
            if(m.find(ntof)!=m.end())
            {
                result.push_back(m[ntof]);result.push_back(i);
                return result;
            }
            m[nums[i]]=i;
        }
        return result;
    }
