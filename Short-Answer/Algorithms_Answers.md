#### Please add your answers to the **_Analysis of Algorithms_** exercises here.

## Exercise I

a) This is O(n) because the while loop relies on 'a', and 'a' scales up with n. Doing the math here, you will see that any number you put in n, the while loop will still run 'n' amount of times, making it O(n)

b) O(nlogn). This is because the while loop only runs logn times of n, mainly because the while loops relies on j, and in the body, j \*= 2 which means it only runs a fraction of the amount of length of n.

After that, we just have a for loop that runs through n, so O(n) there. so Now we just multiply the while loop with the foor loop time complexity and we get O(nlogn)

c) This is O(n), as it's a recursive function that only calls itself once in the body.
Since recursive functions repeat itself based on an input, it's O(n).
Since there are also no other loops in the body, everything else is O(1), leaving with the biggest time complexity being O(n)

## Exercise II
