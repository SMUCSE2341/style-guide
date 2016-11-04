# C++ Style Guide

## Variable, Function, and Class Names

All names should be meaningful, descriptive, and readable.

```{c++}
//Good
int wordCount;

//Bad
int c;
int wrCt;
```

### Variables

Variable names should be camel-case, starting with a lowercase letter.

```{c++}
//Good
int flightCount;

//Bad
int FlightCount;
```

### Functions

Function names should follow the same convention as variables.

```{c++}
//Good
int countFlights();

//Bad
int Count_Flights();
```

### Classes

Classe names should be camel-case, starting with an uppercase letter.
```{c++}
//Good
class FlightPath {};

//Bad
class flightpath {};
```

## Comments

### Inline comments
Inline comments should be expalantory but brief and concise, and should be placed above the line if more than a few words, or can be placed to the right of the line if only about 2-3 words. If placing multiple comments to the side, they should be aligned along the same column.

```{c++}
// Good

// Partition array and return pivot index
int pivot = partition(words, low, high);
quicksort(words, low, pivot - 1);     // Sort left partition
quicksort(words, pivot + 1, high);    // Sort right partition

// Bad

int pivot = partition(words, 0, words.size() - 1);        // This will parition the array, placing the lower elements to the left of the pivot, and the higher elements to the right of the pivot, then it will return pivot index
quicksort(words, low, pivot - 1);  // Sort left partition
quicksort(words, pivot + 1, high);       // Sort right partition
```

## Whitespace


### Indentation
It is up to you whether you want to use 2, 4 or 8 spaces, or tabs, but your choice of style must be consistent.

```{c++}
//Good

int collatz(int n) {
    if (n % 2 == 0)
        return n / 2;
    else
        return 3*n + 1;
}


//Bad
int collatz(int n) {
if (n % 2 == 0)
return n / 2;
  else
     return 3*n + 1;
}
```

### Vertical Whitespace
Use whitespace to group logical steps together.

```{c++}
foo.setBar(1)
foo.setBaz(1)

bar.setBar(1)
bar.setBaz(1)
```

Place 1-2 lines between function declarations.
```{c++}
//Good
double foo(double x) {
    return x * 2;
}

double bar(double x) {
    return x * 3;
}



//Bad
double foo(double x) {
    return x * 2;
}
double bar(double x) {
    return x * 3;
}
```

### Horizontal Whitespace
Open braces should have a space before them, and conditionals should have spaces after the if
keyword and around the else keyword.
```{c++}
void foo() {
    if (flag) {

    } else {

    }
}
```
