# Leetcode’s Roman to Integer  Problem  Solution in (JavaScript)

> The Roman to Integer problem states that given a roman numeral, convert it to an integer. Roman numerals are represented by seven different symbols: I, V, X, L, C, D and M with its values in an object you have to convert them to integers .

# My Solution:
```javascript
function romanToInt(str) {
    const map = {
        I: 1,
        V: 5,
        X: 10,
        L: 50,
        C: 100,
        D: 500,
        M: 1000
    };
    let result = 0;
    for (let i = 0; i < str.length; i++) {
        let curr = map[str[i]];
        let next = map[str[i+1]];
        if (next && curr < next) {
            result -= curr;
        } else {
            result += curr;
        }
    }
    return result;
}
```

# Solution:

> Approach: The approach used in this code is to loop over each letter in the string, adding or subtracting the value of each symbol depending on whether it is greater or less than the next symbol. 

# Algorithm

> The algorithm used is to store each symbol in a lookup table (map) and then loop over the string and add or subtract the value of each symbol based on the result of the comparison. 

# Complexity Analysis

> The overall time and space complexity of this code is O(n), where n is the length of the string.



































