#### Please add your answers to the **_Analysis of Algorithms_** exercises here.

## Exercise I

a) This is O(n) because the while loop relies on 'a', and 'a' scales up with n. Doing the math here, you will see that any number you put in n, the while loop will still run 'n' amount of times, making it O(n)

b) O(nlogn). This is because the while loop only runs logn times of n, mainly because the while loops relies on j, and in the body, j \*= 2 which means it only runs a fraction of the amount of length of n.

After that, we just have a for loop that runs through n, so O(n) there. so Now we just multiply the while loop with the foor loop time complexity and we get O(nlogn)

c) This is O(n), as it's a recursive function that only calls itself once in the body.
Since recursive functions repeat itself based on an input, it's O(n).
Since there are also no other loops in the body, everything else is O(1), leaving with the biggest time complexity being O(n)

## Exercise II

```python
def find_safest_floor(building_floors, left, right):
    if right >= left:

        # Base cases

        if right - left == 1:
            if throw_egg(building_floors[right]) == "broken":
                if throw_egg(building_floors[left]) == "good":
                    return building_floors[left]
        elif right - left == 0:
            return building_floors[left]



        mid = left + (right -1) / 2

        # Check middle floor
        if throw_egg(building_floors[mid]) == "broken":
            # If broken, keep checking left side of the array.
            return find_safest_floor(building_floors, l, mid - 1)


        #Else floor is on the right side of array (higher floor sides)
        return find_safest_floor(building_floors, mid + 1, right)

    else:
        #what?!
        return -1
```

This is a binary search style that has a runtime complexity of O(log n)
This is because it does not have to loop all 'n' amount of times as the nature of binary search.
Binary search will cut half of the floors off at first iteration which drastically decreases any future checks.
Since the function will call itself again, and will cut half of the list again, this keeps reducing the runtime complexity amount, making it O(log n)

<!-- ```python
def find_breaking_floor(building_floors):
    for floor_index in range(0, len(building)):
         if throw_egg(floor_index) == "broken":
             return floor_index
```

This is a very simple solution, it's a linear search to find the first floor that the egg breaks at.
Currently this solution has a runtime complexity of O(n) because the for loop runs n amount of times dependent on the length of the building_floors -->
