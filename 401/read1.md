# Pain vs. Suffering

## refrences

* https://codefellows.github.io/code-401-python-guide/curriculum/class-01/notes/pain_suffering
* https://rob-bell.net/2009/06/a-beginners-guide-to-big-o-notation/
* https://www.codenewbie.org/basecs/8
* https://www.youtube.com/watch?v=_AEJHKGk9ns
* https://towardsdatascience.com/how-to-setup-an-awesome-python-environment-for-data-science-or-anything-else-35d358cc95d5
* https://pymotw.com/3/index.html



## Suffering is pain without purpose. Pain with no higher goal. Pain with no dreams, no ambition, no aspiration.

* As you experience pain, seek the remedy! Ask questions that bridge the gap between what you know and what you need to be able to do. Research! Build your resources and your community! Don’t experience the pain in silence—that slides toward needless pain and the realm of suffering.

Find the common thread that makes the pain worthwhile, that puts the pain into perspective. You’re here because you chose to invest in a different life. A better life.

## A beginner's guide to Big O notation

* Big O notation is used in Computer Science to describe the performance or complexity of an algorithm. Big O specifically describes the worst-case scenario, and can be used to describe the execution time required or the space used (e.g. in memory or on disk) by an algorithm.

## O(1)

* O(1) describes an algorithm that will always execute in the same time (or space) regardless of the size of the input data set.

## O(N)

* O(N) describes an algorithm whose performance will grow linearly and in direct proportion to the size of the input data set. The example below also demonstrates how Big O favours the worst-case performance scenario; a matching string could be found during any iteration of the for loop and the function would return early, but Big O notation will always assume the upper limit where the algorithm will perform the maximum number of iterations.

## O(N2)

* O(N2) represents an algorithm whose performance is directly proportional to the square of the size of the input data set. This is common with algorithms that involve nested iterations over the data set. Deeper nested iterations will result in O(N3), O(N4) etc.

## O(2N)

* O(2N) denotes an algorithm whose growth doubles with each additon to the input data set. The growth curve of an O(2N) function is exponential - starting off very shallow, then rising meteorically. An example of an O(2N) function is the recursive calculation of Fibonacci numbers:

## Logarithms

* Logarithms are slightly trickier to explain so I'll use a common example:

* Binary search is a technique used to search sorted data sets. It works by selecting the middle element of the data set, essentially the median, and compares it against a target value. If the values match it will return success. If the target value is higher than the value of the probe element it will take the upper half of the data set and perform the same operation against it. Likewise, if the target value is lower than the value of the probe element it will perform the operation against the lower half. It will continue to halve the data set with each iteration until the value has been found or until it can no longer split the data set.

* This type of algorithm is described as O(log N). The iterative halving of data sets described in the binary search example produces a growth curve that peaks at the beginning and slowly flattens out as the size of the data sets increase e.g. an input data set containing 10 items takes one second to complete, a data set containing 100 items takes two seconds, and a data set containing 1000 items will take three seconds. Doubling the size of the input data set has little effect on its growth as after a single iteration of the algorithm the data set will be halved and therefore on a par with an input data set half the size. This makes algorithms like binary search extremely efficient when dealing with large data sets.

