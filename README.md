# PACE
For education purpose code from leet code
class Solution {
public:
    vector<int> plusOne(vector<int>& digits) {
        int n = digits.size();
        
        // Traverse from last digit
        for (int i = n - 1; i >= 0; i--) {
            if (digits[i] < 9) {
                digits[i]++;      // just add 1
                return digits;
            }
            digits[i] = 0;        // if digit is 9, make it 0
        }
        
        // If all digits were 9 (e.g., 999 → 1000)
        digits.insert(digits.begin(), 1);
        return digits;
    }
};
