# code-3
class Solution
{
    public:
    //Function to remove common characters and concatenate two strings.
    string concatenatedString(string s1, string s2) 
    { 
        // Your code here
        string res="";
        unordered_map<char,int>mps1;
        unordered_map<char,int>mps2;
        for(int i=0;i<s1.size();i++){
            mps1[s1[i]]++;
        }
        for(int i=0;i<s2.size();i++){
            mps2[s2[i]]++;
        }
        for(int i=0;i<s1.size();i++){
            if(mps2[s1[i]]==0){
                res=res+s1[i];
                
            }
        }
        for(int i=0;i<s2.size();i++){
            if(mps1[s2[i]]==0){
                res=res+s2[i];
                
            }
        }
        return res;
    }

};
