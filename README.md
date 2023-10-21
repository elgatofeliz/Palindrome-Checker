# Palindrome-Checker

    FreeCodeCamp
    JavaScript Algorithms and Data Structures
    JavaScript Algorithms and Data Structures Projects

Palindrome Checker

Return true if the given string is a palindrome. Otherwise, return false.

A palindrome is a word or sentence that's spelled the same way both forward and backward, ignoring punctuation, case, and spacing.

Note: You'll need to remove all non-alphanumeric characters (punctuation, spaces and symbols) and turn everything into the same case (lower or upper case) in order to check for palindromes.

We'll pass strings with varying formats, such as racecar, RaceCar, and race CAR among others.

We'll also pass strings with special symbols, such as 2A3*3a2, 2A3 3a2, and 2_A3*3#A2.


### Code

    function palindrome(str) {
      const workString = str.replace(/[^A-Za-z0-9]/g,'').toLowerCase().split("")
    
      let check = false
    
        for (let i = 0; i < workString.length / 2; i++){
    
          console.log(workString[i], workString[workString.length - i - 1])
          if(workString[i] === workString[workString.length - i - 1]){
            check = true
          }
          if(workString[i] !== workString[workString.length - i - 1]){
            return false
          }
          
        }
    
      return check;
    }
    
    palindrome("1 eye for of 1 eye.");
