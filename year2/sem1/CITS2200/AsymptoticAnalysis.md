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

- Goal is first element in array - *a* units
- Goal is the last element in the array - *a + bn* units;

for some constants *a* and *b*

### Worst Case scenario

Choose which data has the worst time/space requirements.
In the case of eSearch, the worst cast complexity is *a+bn*


