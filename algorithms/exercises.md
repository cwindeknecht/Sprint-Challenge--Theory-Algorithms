## Exercise 1

This should be fun since I haven't taken any math passed algebra, and that was at least 10 years ago...

Sub-Exercise | Answer
---: | :---: 
a) | O(n^3)
b) | O(1/2n) => O(n) 
c) | O(sqrt(n)/2) * 8+i * 8+j) => O(sqrt(n)/2)) => O(n)
d) | O(log n * n) => O(n log n)
e) | O(n * n * n * 10+k) => O(n * n * n) => O(n^3)
f) | O(1^n) so... O(1)? Doesn't seem right at all...
g) | No clue... seems like O(n) or O(1) but doubt it...

## Exercise 2
 
### a)

```
int i = 0;
int j = a.length;
int diff = 0;
while(j > i) {
    int temp = arr[j] - arr[i];
    j--;
    if(temp > diff) diff = temp;
}
```

* Think this would only work with an array sorted (0...n), not sure how to do linear otherwise...
* I suppose it would still be linear if I were to call sort(a) outside of the while loop?

### b)

```
int i, break, n = buildingHeight, egg_threshold = 0;
for(i = 0; i <= n; i++) {
    break = dropEgg();
    if(break == 0) egg_threshold = i;
    else break;
}
```
* dropEgg returns 0 if eggs stays in tact, 1 if it breaks
* this would run until an egg breaks, at which point we should have the highest floor that an egg doesn't break stored in the egg_threshold variable.

## Exercise 3

(I admittedly am terrible with understanding the need for pivots or why quicksort is so much better than other sorting algorithms.  I will research this more in the afternoon.  I looked into this, I didn't "know" them).

### a) 

This would be O(n^2) because the pivot would be the lowest number.

### b)

This seems like it would be best/average case, both of which are O(n log n).  As to exactly why, I couldn't tell you...