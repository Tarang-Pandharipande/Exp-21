**Aim:**  
To explore and implement Searching algorithms.  
<br>
**Theory:**  
Searching is the process of locating a specific element or value within a dataset. In this experiment, we will study two types of searching algorithms:  
&#8594; Linear Search  
&#8594; Binary Search  
<br>

_Linear Search:_ In linear search, the elements in the collection are inspected one by one until the desired element is found or the search ends. This algorithm doesn’t require the data to be sorted. Its time complexity is O(n), where n is the number of elements in the dataset.  
Linear Search Steps:  
1. Begin at the first element in the array.  
2. Compare the current element with the target.  
3. If they are the same, return the index of the current element.  
4. If they differ, move to the next element.  
5. Continue this process until either the element is found or the end of the array is reached.  
<br>

_Binary Search:_ Binary search is a more efficient algorithm but requires the dataset to be sorted. The method works by repeatedly dividing the array into two halves to determine if the target element is in the left half or the right half. It has a time complexity of O(log n), where n represents the number of elements in the dataset.  
Binary Search Steps:  
1. Compare the target value to the middle element of the array.  
2. If the target matches the middle element, return the index.  
3. If the target is smaller, search the left half of the array.  
4. If the target is larger, search the right half of the array.  
5. Repeat this process until the target is found or the sub-array size becomes zero.  
<br>
**Code:** <br>
<br>
a.<br>

```
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

```
<br>
b.<br>

```
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

```
<br>


**Outputs:**  <br>
<br>
a.<br>
![exp21a output](https://github.com/tanishaamenon/CDS---Searching/blob/main/exp21a.JPG) <br>
b.<br>
![exp21b output](https://github.com/tanishaamenon/CDS---Searching/blob/main/exp21b.JPG) <br>
<br>

**Conclusion:** <br>
&#8594; We learnt about searching in C++. <br>
&#8594; We learnt the use case of the types of searching in C++. <br>
*******
<br>
