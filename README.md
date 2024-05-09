# CheckPrime
Checking prime numbers is a simple and easy problem to solve through programming through multiple ways. However, not all the ways are time efficient. This method uses mathematical principles to solve this problem.
The mathematical logic behind using the condition `i * i <= n` in the `while` loop to check for prime numbers is based 
on optimization and the properties of divisors.
When checking if a number `k` is prime, we only need to test divisibility up to its square root (√k). This is because:
• If `k` is not a prime number, it can be factored into two factors, `a` and `b`, where both `a` and `b` are greater 
than 1 and less than `k`. 
• If both `a` and `b` were greater than the square root of `k`, their product (`a * b`) would be greater than `k`, 
which is not possible because `k` is the maximum value.
For example: Suppose we're testing whether `k = 100` is prime:
• The divisors of 100 are: 1, 2, 4, 5, 10, 20, 25, 50, 100. 
• Notice that all divisors less than or equal to √100 = 10 are paired with divisors greater than √100. For 
example, 1 is paired with 100, 2 is paired with 50, and so on. 
• If a divisor `a` is greater than √100, its corresponding divisor `b` would be less than √100, and vice versa.
• Based on this observation, we can conclude that if no divisors are found up to √k, there will be no divisors 
greater than √k that will divide `k` either. 
• Therefore, we can optimize the prime number check code by only testing divisors up to √k.
In terms of the `while` loop condition `i * i <= k`, as long as `i * i` is less than or equal to `k`, the loop continues to 
check divisors. Once `i * i` exceeds `k`, it's not necessary to continue because any potential divisors greater than √k 
would have already been checked on the other side of the square root.
This optimization significantly reduces the number of divisor checks and makes the primality test more efficient.
Let's use the example of checking whether the number 17 is prime using the condition `i * i <= k` in the `while` loop.
1. We want to check if 17 is a prime number.
2. The square root of 17 is approximately 4.123.
3. In the loop, we start checking potential divisors from 2 (i = 2).
4. When i = 2, i * i = 4, which is less than or equal to 17. So, we continue to check.
5. When i = 3, i * i = 9, which is less than 17. We continue.
6. When i = 4, i * i = 16, which is less than 17. We continue.
7. When i = 5, i * i = 25, which is greater than 17. We stop the loop because we exceeded the square root of 17.
Since we found no divisors of 17 up to its square root, we can conclude that 17 is a prime number. This is based on 
the logic that if 17 were not a prime number, it would have factors that are less than or equal to 4, which we have 
already checked.
The use of `i * i <= k` optimizes the process by avoiding unnecessary divisor checks for values greater than the square 
root of the number being tested. This optimization becomes even more pronounced for larger numbers, where the 
number of potential divisors is significantly reduced by limiting the search to the square root.
