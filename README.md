Implement strStr()
=====


public class Solution {
    public String strStr(String haystack, String needle) {
        
        if(haystack.equals(needle) || needle=="")
            return haystack;
        else
            for(int i=0;i<haystack.length()-1;i++)
            {
                if((haystack.substring(i,i+1)).equals(needle.substring(0,1)))
                {
                    int len = i+ needle.length();
                    if(len>haystack.length())
                        return null;
                    else
                    if((haystack.substring(i,i+needle.length())).equals(needle))
                        return haystack.substring(i,haystack.length());
                }
            }
        
        return null;
    }
}
