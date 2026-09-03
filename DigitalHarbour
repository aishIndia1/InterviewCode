// Given two strings s and t of lengths m and n respectively, return the minimum window 
// substring
//  of s such that every character in t (including duplicates) is included in the window. 
// If there is no such substring, returnthe empty string "".The testcases will be generated such that the answer is unique.
// Example 1:
// Input: s = "ADOBECODEBANC", t = "ABC"
// Output: "BANC"
// Explanation: The minimum window substring "BANC" includes 'A', 'B', and 'C' from string t.
// Example 2:
// Input: s = "a", t = "a"
// Output: "a"
// Explanation: The entire string s is the minimum window.
// Example 3:
// Input: s = "a", t = "aa"
// Output: ""
// Explanation: Both 'a's from t must be included in the window.
// Since the largest window of s only has one 'a', return empty string.
public class Main {

    public static void main(String[] args) {
        System.out.println("Hello, World!");

        String s = "ADOBECODEBANC";
        String t = "ABC";

        if(t.length() > s.length()){
            System.out.println("");
        }

        int[] freq = new int[128];

        for(char c: t.toCharArray()){
            freq[c]++;
        }

        int left=0, right=0, count=t.length();
        int start = 0;
        int minLength = Integer.MAX_VALUE;

        // freq[] = {A-1, B-1, C-1}
        // s = ADOBECODEBANC
        for(right=0; right<s.length(); right++){
            char ch = s.charAt(right);

            if(freq[ch] > 0){// freqD < 0
                count--; 
            }
            freq[ch]--;// freqD=-1
            
            while(count == 0){
                if(right - left + 1 < minLength){
                    minLength = right - left +1;
                    start = left;
                }
            

            char leftChar = s.charAt(left); //A

            freq[leftChar]++; //freqA=1

            if(freq[leftChar] > 0){ 
                count ++;// count 3 
            }

            left++; //1
        }
        }
        

        String result = s.substring(start, start+minLength);

        System.out.println(result);

        // Your code here
    }
}
