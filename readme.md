## Palindrome Checker

### Overview
This is a simple web application that checks whether a given word or phrase is a palindrome or not. A palindrome is a word, phrase, number, or other sequence of characters that reads the same forward and backward (ignoring spaces, punctuation, and capitalization).

### Technologies Used
- HTML
- CSS
- JavaScript

### How to Use
1. Clone this repository to your local machine.
2. Open `index.html` in your web browser.
3. Enter a word or phrase into the input field.
4. Click the "Check" button.
5. The result will be displayed below the input field, indicating whether the input is a palindrome or not.

### Features
- Case-insensitive: The program ignores capitalization, so "Racecar" and "racecar" are considered the same.
- Handles phrases: Spaces and punctuation are ignored, so "A man, a plan, a canal, Panama!" is recognized as a palindrome.

### Code Structure
- `index.html`: Contains the structure of the web page.
- `style.css`: Contains the styles for the web page.
- `script.js`: Contains the JavaScript code for checking palindromes.
  
### Code Sample
```javascript
function isPalindrome(str) {
    // Remove non-alphanumeric characters and convert to lowercase
    let alphanumericStr = str.replace(/[^0-9a-z]/gi, '').toLowerCase();
    // Reverse the string
    let reversedStr = alphanumericStr.split('').reverse().join('');
    // Check if the original and reversed strings are equal
    return alphanumericStr === reversedStr;
}

function checkPalindrome() {
    let input = document.getElementById('input').value;
    let result = document.getElementById('result');
    if (isPalindrome(input)) {
        result.innerText = "Palindrome!";
    } else {
        result.innerText = "Not a Palindrome!";
    }
}
```

### Demo
![Demo](demo.gif)

### License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

### Acknowledgments
- Inspired by the concept of palindromes.