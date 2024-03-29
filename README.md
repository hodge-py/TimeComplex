# TimeComplex

This package was created to evaluate functions for time complexity. The function runs an algorithm over and over with randomized input sizes to judge the time complexity.
PYPI:
<https://pypi.org/project/SpaceTimeComplex/>

## Example

```python

import TimeComplex

def looper2(n):
    for x in range(n):
        print(x)

def testone(n):
    for x in range(len(n)):
        for y in range(len(n)):
            for z in range(len(n)):
              two = y
              one = x
              three = z

def looper(today,stringer):
    for x in range(today):
        print(x)
    
    for y in stringer:
        print(y)



def logfunc(n):
    for x in range(0,len(n[0]),20):
        print(x) 


def binary_search(array,target):
  low = 0
  high = len(array) - 1
  while low <= high:
    mid = (low + high) // 2 # integer division
    element = array[mid]
    if element == target:
      return mid
    elif element < target:
      low = mid + 1
    else:
      high = mid - 1
  return -1


real = TimeComplex.RealTime() # Create the class
#x.realTimeComplex(stmt="looper(10)",value=10)

testSet = real.generateTestSet(size2=100) #generate a test set

testSet1 = [[4,"stnr=gwege"], [12,"sagsdgg"], [3,"esfsfsseafesfsefsef"], [45,"stnrefgseege"], [17,"sagwetjtwfwe"], [34,"esfsfssem"],[41,"stn"], [53,"sakhhksdgg"], [24,"esjfjkkfsefsef"], [70,"stnwete"], [7,"sagwefwewsdfsdffwe"] ] 
# format of array. 2d array with each test set inside. You can make your own or just generate one with generateTestSet()

logFunction, SlopeConst = real.complexGuess(testone,testSet) #guess the complexity of a function. Returns the guess and a plot

ratio = real.bestWorst(testone,testSet)

```

![figureex](https://github.com/hodge-py/TimeComplex/assets/105604814/a59a49ab-1aa3-48d6-80e3-fe3d68ef33f5)

![firgurehist](https://github.com/hodge-py/TimeComplex/assets/105604814/48ac6f25-91ac-4163-adac-5cfe8f8c710c)

![finaloutput](https://github.com/hodge-py/TimeComplex/assets/105604814/97450568-cd8f-4a6d-9c6c-d666dfa6c9c8)

## Example of the non-log function graphed using the derived power. $O(n^{2.8})$

![grapher](https://github.com/hodge-py/TimeComplex/assets/105604814/028554a6-36c5-431f-b1ba-58bdd0a23223)

This is in respects to time (ms). When accounting for just the growth of input, the input will grow in a polynomial fashion.

## Math behind the calculations

A simplistic understanding how the time complexity is extracted stems from the log power rule.

Power Rule:

$log(n^k) = k \cdot log(n)$

After apply a log to both n and y variables, a linear regression is applied.

$y = time, n = input size, b = constant$

$log(y) = log(n^k) + b$

apply the power rule

$log(y) = k \cdot log(n) + b$

Everything can be ignored except for k. k determines the slope of line and tells us the time complexity.

$time complexity = N^k$

## Jupyter Lab

The package can also be used in jupyter notebooks.
