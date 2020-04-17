#### Please add your answers to the ***Analysis of  Algorithms*** exercises here.

## Exercise I

a) O(n) only one loop iterating


b) O(n^2) one loop iterating within another.


c) O(n) recusion running esstialy a single while loop

## Exercise II

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

runtime would be O(n^2) because of nested for loop