1. **What was the bug?**
    - The bug was that the `num1` and `num2` were `strings`. Therefore, the code just combines two strings instead of adding two integers. 
2. **How would you fix it? Include a screenshot of your fix.**
    - The bug can be fixed by making `num1` and `num2` integers by using `Number(num1)` and `Number(num2)` before calculating the result.