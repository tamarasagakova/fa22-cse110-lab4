1. **What will happen at line 12 and why? If the code causes an error, explain why.**
   - Line 12 will print `3` since `i` was decalread as `var` and can be called out of the block scope it was delared in. `3` was the last value assigned to `i`.
2. **What will happen at line 13 and why? If the code causes an error, explain why.**
    - Line 13 will print `150` since `discountedPrice` was decalread as `var` and can be called out of the block scope it was delared in. `150` was the last value assigned to `discountedPrice` since `300 * (1 - 0.5) = 150`.
3. **What will happen at line 14 and why? If the code causes an error, explain why.**
    - Line 14 will print `150` since `finalPrice` was decalread as `var` and can be called out of the block scope it was delared in. `150` was the last value assigned to `finalPrice` since `(150 * 100) / 100 = 150`.
4. **What will this function return? Give a brief explanation why. If the code causes an error, explain why.**
    - The function will return an array `[50, 100, 150]`. During the for loop, we push the value of the `finalPrice` into this array each round. Then line 16 returns the array.
5. **What will happen at line 12 and why?  If the code causes an error, explain why. (assume this function is being called like the others: discountPrices([100, 200, 300], 0.5)).**
    - The code causes an error due to the fact that `i` defined using `let`; therefore, it can be accessed only inside the block it was defined in. Meaning it can not be used outside of the for loop.
6. **What will happen at line 13 and why? If the code causes an error, explain why.**
    - The code causes an error due to the fact that `discountedPrice` defined using `let`; therefore, it can be accessed only inside the block it was defined in. Meaning it can not be used outside of the for loop.
7. **What will happen at line 14 and why? If the code causes an error, explain why.**
    - Line 14 will print `150` since `finalPrice` was decalread as `let` and we are calling it inside the block scope. `150` was the last value assigned to `finalPrice` since `(150 * 100) / 100 = 150`.
8. **What will this function return? Give a brief explanation. If the code causes an error, explain why.**
    - The function will return an array `[50, 100, 150]`. During the for loop, we push the value of the `finalPrice` into this array each round. Then line 16 returns the array. We are using `let` this time, but since the variables are accessed inside the block scope, everything works perfectly.  
9.  **What will happen at line 11 and why? If the code causes an error, explain why.**
    - The code causes an error due to the fact that `i` defined using `let`; therefore, it can be accessed only inside the block it was defined in. Meaning it can not be used outside of the for loop.
10. **What will happen at line 12 and why? If the code causes an error, explain why.**
    - Line 12 will print `3` since `length` was decalread as `const` and was assigned once, so it keeps the length of `prices` which is `3`.
11. **What will this function return? Give a brief explanation. If the code causes an error, explain why.**
    - The function will return an array `[50, 100, 150]`. Even though we use `const` to define `discounted`, we still can push values in it. `const` cannot be reassined, but can have new values push into.
12. **Given the above Object, write the notation for:**
    
    **A. Accessing the value of the name property in the student object**
    - student.name;
- 
    **B. Accessing the value of the Grad Year property in the student object**
    - student["Grad Year"];
    
    **C. Calling the function for the greeting property in the student object**
    - student.greeting();
    
    **D. Accessing the name property of the object in the Favorite Teacher property in student**
    - student['Favorite Teacher'].name;
    
    **E. Access index zero in the array of the courseLoad property of the student object**
    - student.courseLoad[0];
13. **Arithmetic**
    
    **A. ‘3’ + 2**
    - `'32'` (string). Here the plus sign is used to combine two strings and it automatically coverts `2` to a string.  

     **B. ‘3’ - 2**
    - `1` (integer). Minus sign is a `math operator` and it converts `'3'` to an integer.
    
    **C. 3 + null**
    - `3` (integer). Here `null` is coverted to `0`, which makes `3 + 0 = 3`. 
    
    **D. ‘3’ + null**
    - `'3null'` (string). Here the plus sign is used to combine two strings, so it combines them into `'3null'`.
    
    **E. true + 3**
    - `4` (integer). Here the plus sign works as a `math operator` since there are no `strings`. `true` is convereted to `1`, which makes `1 + 3 = 4`.
    
    **F. false + null**
    - `0` (integer). Here the plus sign works as a `math operator` since there are no `strings`. Both `false` and `null` convereted to `0`, which makes `0 + 0 = 0`.
    
    **G. '3' + undefined**
    - `'3undefined'` (string). Plus sign is used to combine two strings, so it converts `undefined` into a string and combines them into `'3undefined'`.
    
    **H. '3' - undefined**
    - `NaN`. Minus sign is a `math operator`, but `undefined` makes it `NaN` because it does not convert to any number.
14. **Comparison**
    
    **A. ‘2’ > 1**
    - `True`. `'2'` is converted to an integer and `2 > 1`. 

    **B. ‘2’ < ‘12’**
    - `False`. Since they are compared as strings using lexicographical order and sorts numbers alphabetically, `'2' > '12'`.
    
    **C. 2 == ‘2’**
    - `True`. `'2'` is converted to an integer and `2 == 2`.
    
    **D. 2 === ‘2’**
    - `False`. `===` doesn't convert anything, therefore, an integer is not equal to a string. 
  
    **E. true == 2**
    - `False`. `true` is converted to `1` and `1` does not equal to `2`.
    
    **F. true === Boolean(2)**
    - `True`. `Boolean()` converts non empty value to `true` and `true === true`.
15. **Explain the difference between the == and === operators.**
    - `==` checks the variables with conversions (ignores datatypes), while `===` checks the variables, as well as, their datatypes(without converstion).
16. **Can be found in `part2-question16.js`**
17. **If the function above is called with the following parameters modifyArray([1,2,3], doSomething), what will be the result? Briefly walk through how you arrived at that result. Here we are passing in a function as a parameter, however we can also return a function from another function just as easily, you're encouraged to play around with callbacks as they are used heavily in frontend JS development.**
    - The result will be `[2,4,6]`. Line 13 calls `modifyArray([1,2,3], dosomething)` which causes `newArr` push values of `callback(array[i])`. Then `dosomething(array[i])` returns each `num` multiplied by 2, which is basically `array[i]*2`. At the end we return `newArr`, which is `[2,4,6]`.
18. **Can be found in `part2-question18.js`**
19. **What is the output of the above code?**
```
1
4
3
2
```
