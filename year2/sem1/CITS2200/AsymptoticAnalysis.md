# Asymptotic Analysis
---
## Worst Case vs Expected Case

Abstract measures of performance will still depend on actual input data


eg. Exaustive Sequential Search
```java
public int eSearch(...){
    ...
    i = 0;
    while (a[i] != goal && i < n){
        i++;
    }
    if (i==n){      //Goal not found
        return -1;
    }
    else{
        return i;
    }
}
```
## Abstract time

- Goal is first element in array - $a$ units
- Goal is the last element in the array - $a + bn$ units;

for some constants $a$ nd $b$

### Worst Case scenario

Choose which data has the worst time/space requirements.
In the case of eSearch, the worst cast complexity is $a+bn$

#### Advantages

- Reletivly Simple
- Gives upperbound or garrentee of behaviour/can't preform worse
  

#### Disadvantages

- Worst case could be unrepresentative of realistic results
- Can't get anyone to buy it

Since we want behavior garrentees we will usually consider worst case scenario

(note there is also best case scenario such as car salesmen or stock brokers)

### Expected Case Analysis

What happens on the average or expected case.
For `eSearch`, $a+$$bn \over 2$ assuming a uniform distribution of input.

#### Advantages
- More realistic indicator
- Reduces affects of outlier samples
eg. `QuickSort` is usually the fastest even though it has worst time complexity.

#### Disadvantages

- Only possible if we know the distribution over examples
- More difficult to calculate
- Often does not provide significanty more information than worst case scenario
- May be misleading
