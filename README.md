# leetcode-Pancake-Sorting-Solution
in cpp 
class Solution {
public:
     vector<int>v;
    vector<int> pancakeSort(vector<int>& A) {
       for(int i=A.size();i>0;i--)
           flip(A,i);
        return v;
        
    }
    void flip(vector<int>&a,int i)
    {
        int j=0;
        if(a[i-1]==i)
            return ;
        else
        {
            for(j=0;j<a.size();j++)
            {
                if(a[j]==i)
                {
                    break;
                }
            }
            reverse(a.begin(),a.begin()+j+1);
                v.push_back(j+1);
             reverse(a.begin(),a.begin()+i);
            v.push_back(i);
        }
    }
};
