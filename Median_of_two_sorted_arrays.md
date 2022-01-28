# data-structure-and-algorithm
my data structure and algorithms questions solutions
Q 2:-  Given two sorted arrays nums1 and nums2 of size m and n respectively, return the median of the two sorted arrays.

The overall run time complexity should be O(log (m+n)).

 

Example 1:

Input: nums1 = [1,3], nums2 = [2]
Output: 2.00000
Explanation: merged array = [1,2,3] and median is 2.

              -:Algorithm:-
 > Start
 > Reads both of arrays and store them in a new declared array
 > sort the array
 > find the median apply the following formula: if N=even then Median = [(n/2)th term + ((n/2)+1)th term]/2;
                                                if N=odd then Median = [(n+1)/2]th term;
 > return the value
 > End
 
              -:Code:-
              
   double findMedianSortedArrays(vector<int>& nums1, vector<int>& nums2) {
       vector<int> a;
        for(int i=0;i<nums1.size();i++)
        {
            a.push_back(nums1[i]);
        }
        for(int i=0;i<nums2.size();i++)
        {
            a.push_back(nums2[i]);
        }
        int n=a.size()-1;
        sort(a.begin(),a.end());
        if(a.size()%2==0)
        {
            return (a[n/2]+a[(n+1)/2])/2.00;
        }else {
            return a[(n+1)/2];
        }
    }
 
 
