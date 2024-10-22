# EXPERIMENT-21
# searching
# AIM- To study and implement searching in c++
# Theroy-
Searching: Overview
Searching is the process of finding the location of a specific element within a data collection. Two widely used search algorithms are Linear Search and Binary Search.

Linear Search
Linear search, also known as sequential search, checks each element in a collection one by one until the target is found or the search ends. It works on both sorted and unsorted data.

Steps of Linear Search:
Start at the first element.
Compare the target with the current element.
If they match, return the index. Otherwise, move to the next element.
Repeat until the target is found or the end is reached.
Time Complexity:
O(n) – In the worst case, it will check all n elements, making it inefficient for large datasets.

Binary Search
Binary search is much faster but requires the data to be sorted. It works by repeatedly dividing the collection in half to narrow down the search.

Steps of Binary Search:
Find the middle element of the array.
Compare the target with the middle element.
If it matches, return the index.
If the target is smaller, search the left half.
If larger, search the right half.
Repeat until the target is found or the search space is empty.
Time Complexity:
O(log n) – Each step halves the search space, making it highly efficient for large datasets.

Comparison:
Linear Search: Works on unsorted data but is slower (O(n)).
Binary Search: Faster (O(log n)) but requires sorted data
# Code-
~~~
a.
#include <iostream>
using namespace std;

int linsearch(int a[], int n, int x)
{
    for (int i = 0; i < n; i++)
        if (a[i] == x)
            return i;
    return -1;
}

int main(void)
{
    int a[] = { 21, 36, 44, 10, 57 };
    int x = 10;
    int n = sizeof(a) / sizeof(a[0]);


    int res = linsearch(a, n, x);
    (res == -1)
        ? cout << "Element is not present in aay"
        : cout << "Element is present at index " << res;
    return 0;
}
~~~
b.
~~~
#include <iostream>
using namespace std;

int binsearch(int a[], int low, int high, int x)
{
    while (low <= high) 
    {
        int mid = low + (high - low) / 2;

        if (a[mid] == x)
            return mid;

        if (a[mid] < x)
            low = mid + 1;

        else
            high = mid - 1;
    }

    return -1;
}

int main(void)
{
    int a[] = { 32, 87, 14, 92, 45 };
    int x = 14;
    int n = sizeof(a) / sizeof(a[0]);
    int res = binsearch(a, 0, n - 1, x);
    if(res == -1) cout << "Element is not present in array";
    else cout << "Element is present at index " << res;
    return 0;
}
~~~
# Output-
![](https://github.com/SunidhiChoubey/searching/blob/main/Screenshot%202024-10-22%20140009.png)
# Conclusion-
We learnt about searching in C++ and We learnt the use case of the types of searching in C++.


