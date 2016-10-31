# C++ Style Guide

## Variable, Function, and Class Names

All names should be meaningful, descriptive, and readable.

```
//Good
int wordCount;

//Bad
int c;
int wrCt;
```

### Variables

Variable names should be camel-case, starting with a lowercase letter.

```
//Good
int flightCount;

//Bad
int FlightCount;
```

### Functions

Function names should follow the same convention as variables.

```
//Good
int countFlights();

//Bad
int Count_Flights();
```

### Classes

Classe names should be camel-case, starting with an uppercase letter.
```
//Good
class FlightPath {};

//Bad
class flightpath {};
```

## Comments

### Inline comments
Inline comments should be expalantory but brief and concise, and should be placed above the line if more than a few words, or can be placed to the right of the line if only about 2-3 words. If placing multiple comments to the side, they should be aligned along the same column.

```
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

