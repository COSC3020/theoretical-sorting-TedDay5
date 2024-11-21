# Theoretical Sorting

A Computer Science researcher claims to have come up with a sorting algorithm
that can sort arbitrary elements in $O(n)$ time based on comparisons of two
elements at a time. This would be asymptotically faster than any known general
sorting algorithm. The algorithm itself is proprietary and will be sold by a
company.

How would you verify this claim? You may assume that you have access to a
black-box implementation of the sorting algorithm, i.e. you cannot examine the
source code, but you can use it to sort any list you like. Explain in detail
your method for investigating whether X is correct, including any expected
results you would get.

Also give a theoretical argument for why X could or could not be correct, based
on the complexity of the general sorting problem we covered in class.

Add your answers to this markdown file.

If the sorting algorithm could sort in $O(n)$ time, the time would increase linearly whenever the input size, n, increases.
We would be able to test this by giving it a small list and large list, and timing how long each takes, and see if it works with different sizes of lists.
Test by giving different cases, sorted lists, unsorted lists, reverse sorted lists, give it different types such as intergers, strings, single characters to figure out it grows linearly no matter the type of element given.
Also test by seeing what happens when there's multiple of the same values as elements within the lists.
By testing and timing each of these cases we should be able to figure out if it truely increases in $O(n)$ time.
Running each of these tests multiple times to make sure the values are consistant.
While running these tests, it should be all on the same machine, while minimizing the amount of other programs running concurently, all to reduce the constant factors and dropped lower order terms that affect time complexity.
If after all these tests are successful, and the time does increase linearly with the input size, we could say it indeed sorts in $O(n)$ time.

Within the lecture 01 sorting slides, slide 45 it goes over the general complexity of a sorting problem.
The general complexity of a sorting problem we covered in class was $\ohm(nlogn)$ which is true for any comparison based sorting algorithm.
You can show this with a tree, where each possible ordering of an array is a leaf and decision points / comparisons are the branches.
If an array needs to be sorted that's size n, then there must be n! leaves on the tree since there are n! possible permutations of the array.
This means the number of leaves is n!.
If the sorting algorithm x has a $O(n)$ run time, it wouldn't be able to correctly sort the elements since it needs to be able to access all of the leaves, and not have leaves missing.
Since there are n! leaves, it's not possible to be done in $O(n)$ time.
This means X is not correct.
