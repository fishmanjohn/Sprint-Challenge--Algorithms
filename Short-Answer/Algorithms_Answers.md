#### Please add your answers to the ***Analysis of  Algorithms*** exercises here.

## Exercise I

a) O(n) only one loop iterating


b) O(logn) because the 


c) O(n) recusion running esstialy a single while loop

## Exercise II

<!-- 
THIS WAS NOT THE ANSWER...
are the floors orgonised cronologicly i.e. 012345->N or is this some Mc.Esher type building where the list of 
floors is shuffled i.e. 0,2,8,12,3,420,69->N

based on a nomal order of building floors I would iterate over the list of floors 

making_an_omlette_for_f(n,f)
    while eggs are safe:
        for floor in n: 
    >>> an if/else statement would handle checking if the eggs were damaged or not.
            if n[floor] > f:
                eggs are no longer safe
            else:
                eggs are still safe continue itterating up building.

in the hypothetical 4th dimention building where phisics does not apply to floor numbering I wouuld sort first to restore order
then proceeed as planned.

runtime would be O(n^2) because of nested for loop -->

the trick of this question is to halve the number of floors recursively until you find the highest possible floor to drop an egg from

omletteRecursion(n):
    if length of n is equal to or less than one:
        return n
    else:
        midpoint = the length of n floor diveded by 2
        bottom half = n[:midpoint]
        top half = n[midpoint:]

        if n[midpoint] >= f i.e. if the egg breaks:
            omletteRecusion(bottom half) >>> pass the bottom half back into the algorithim and start over with the smaller array

        else if n[midpoint] <= f i.e. if the egg does not break the f floor must be above the half way point of our building array  
            omletteRecusion(top half) >>> pass back in and start over with the smaller array that contains f.

eventualy after recursing over the array sevral times we will have whittled down the aray to passing in an array with a single index 
which is when we hit our base case and return that single index which will be the f floor. Giving us a time complexity of O(log n)