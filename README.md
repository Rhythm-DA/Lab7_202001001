# Lab7_202001001

## Section-A

### TestCases
|ID |Month|Day|Year|Expected Output|
|---|-----|---|----|---------------|
|1  | 2   | 23|2014| Valid         |
|2  | 5   | 32|2000| Invalid       |
|3  | 7   | 29|2018| Invalid       |
|4  | 9   | 13|2008| Valid         |
|5  | 10  | 18|2002| Valid         |
|6  | 24  | 1 |1989| Invalid       |
|7  | 9   | 5 |1999| Valid         |
|8  | 11  | 13|2004| Valid         |
|9  | 12  | 6 |2008| Invalid       |
|10 | 9   | 24|1222| Invalid       |


### Equivalence Class
Day:<br />
|ID| Class   | Validity|
|--|-------  |---------|
|E1| dd<1    | InValid |
|E2|1<=dd<=28| Valid   |
|E3| dd=31   | Valid   |
|E4| dd=29   | Valid   |
|E5| dd=30   | Valid   |
|E6| dd>31   | InValid |

Month:<br />
|ID|             Class                      | Validity|
|--|----------------------------------------|---------|
|E1| mm<1                                   | InValid |
|E2| mm= 1,3,5,7,8,10,12(Month with 31 days)| Valid   |
|E3| mm= 4,6,9,11(Month with 30 days)       | Valid   |
|E4| mm=2(Month with 28 or 29 days)         | Valid   |
|E5| mm>12                                  | InValid |


Year:<br />
|ID|            Class             | Validity|
|--|------------------------------|---------|
|E1| yy<1900                      | InValid |
|E2|leap year 1990<=yy<=2015      | Valid   |
|E3|non leap year 1990<=yy<=2015  | Valid   |
|E4| yy>2015                      | InValid |

## Program 1

### Equivalence Partition For linear Search

| Tester Action and Input Data | Expected Outcome|
|------------------------------|-----------------|
|[2, 4, 6, 8, 10],v = 2	       |     0           |
|[1, 3, 5, 7, 9],v = 2	       |     -1          | 
|[2, 4, 6, 8, 10],v = 11	     |     -1          |
|[-100, 100]	                 |      0          |
|[1,2,3,4,5,6],v = 6	         |      5          | 
|[],v = 10	                   |      -1         |
|NULL,v = 111	                 |      -1         |

### Boundary Value Analysis

| Tester Action and Input Data | Expected Outcome |
|------------------------------|------------------|
| NULL | -1 |
| [],v = 5 | -1 |
| [5],v = 5 | 0 |
| [5],v = 60 | -1 |
| [3,5],v = 3 | 0 |
| [3,5],v = 5 | 1 |
| [3,5],v = 14 | -1 |
| [1,3,5],v = 1 | 0 |
| [1,3,5],v = 5 | 2 |
| [1,3,5],v = 10 | -1 |
|[1,2,3,4,5,6,7,8,9,1,0,11,111],v = 1| 0 |
|[1,2,3,4,5,6,7,8,9,1,0,11,111],v = 111| 12 |
|[1,2,3,4,5,6,7,8,9,1,0,11,111],v = 1111| -1 |

## Program 2

### Equivalence Class partitioning for counting occurance
| Tester Action and Input Data | Expected Outcome |
|------------------------------|------------------|
| [265, 41, 60, 80, 100],v = 100 | 1 |
| [2655, 451, 6560, 1050, 1050],v = 1050 | 2 |
| [[265545, 451, 65460, 1050, 105024]],v = 1 | 0 |
| [[10,10,10,10]],v = 11 | 0 |
| [],v = 100 | 0 |
| NULL,v = 51 | 0 |
| [0],v = 0 | 1 |
| [-89,-89],v = -89 | 2 |

### Boundary value analysis
| Tester Action and Input Data | Expected Outcome |
|------------------------------|------------------|
| [1, 2, 3, 4],v = 2 | 2 |
| 15, 10, 15, 15],v = 15 | 3 |
| [],v = 100 | 0 |
| NULL,v = 51 | 0 |
|[-100,100,100,100],v = 10000| 0 |
| [-89,89],v = -89 | 1 |
| [-890,890],v = 890 | 1 |

## Program 3

### Equivalent testcases for binary search
| Tester Action and Input Data | Expected Outcome |
|------------------------------|------------------|
| [1, 21, 30, 40, 50],v = 21 | 1 |
| [10, 20, 30, 40, 50, 60],v = 30 | 2 |
| [10,100,1000,10000],v = 100000 | -1 |
| [,11,22,33,44],v = 444 | -1 |
| [11,20,200,300],v=11 | 0 |
| [-100,-90,-80,100,1000],v = 10000 | 4 |
| [],v = 12 | -1 |
| NULL,v = 168 | -1 |
| [1,2],v = 3 | -1 |
| [1,3],v=3 | 1 |

### Boundary value analysis
| Tester Action and Input Data | Expected Outcome |
|------------------------------|------------------|
| [1, 2, 3, 4, 5],v = 2 | 1 |
| [1, 2, 2, 351, 551],v = 2 | 2 |
| [1,22,33,44,55],v = 66 | -1 |
| [2, 4, 6, 8, 10],v = 51 | -1 |
| [-100, 0, 1000],v = -100 | 0 |
| [-100, 0, 1000],v = 1000 | 2 |
| [],v=0 | -1 |
| NULL,v = 4 | -1 |

## Program 4

### Equivalent class test cases of checking the type of triangle
| Tester Action and Input Data | Expected Outcome |
|------------------------------|------------------|
| a=2,b=2,c=2 | EQUILATERAL |
| a=1,b=1,c=1 | EQUILATERAL |
| a=0,b=0,c=0 | INVALID |
| a=-1,b=-1,c=-1 | INVALID |
| a=10,b=10,c=0 | INVALID |
| a=17,b=17,c=5 | ISOCELES |
| a=15,b=2,c=15 | ISOCELES |
| a=6,b=11,c=5 | SCALENE |
| a=16,b=21,c=25 | SCALENE |
| a=-1,b=21,c=25 | INVALID |
| a=2,b=3,c=4 | SCALENE |

### Boundary value analysis
| Tester Action and Input Data | Expected Outcome |
|------------------------------|------------------|
| a=2,b=2,c=2 | EQUILATERAL |
| a=0,b=0,c=0 | INVALID |
| a=INT_MAX,b = INT_MAX,c = INT_MAX | EQUILATERAL |
| a=INT_MIN,b=INT_MIN,c=INT_MIN | INVALID |
| a=1,b=1,c=2 | ISOCELES |
| a=15,b=12,c=15 | ISOCELES |
| a = INT_MAX,b = 1,c = INT_MAX | ISOCELES |
| a=1,b=2,c=3 | SCALENE |
| a = INT_MAX,b = 1,c = INT_MAX - 1 | SCALENE |

## Program 5

### Equivalent test cases for prefix searching are as follows
| Tester Action and Input Data | Expected Outcome |
|------------------------------|------------------|
| s1= "abcd",s2 = "abcd" | true |
| s1 = "",s2 = "" | true |
| s1 = "po",s2 = "poojan" | true |
| s1 = "poo",s2 = "po" | false |
| s1 = "abc",s2 = "" | false |
| s1 = "",s2 = "abc" | true |
| s1 = "o",s2 = "ott" | true |
| s1 = "abc",s2 = "def" | false |
| s1 = "deg",s2 = "def" | false |

### Boundary value analysis
| Tester Action and Input Data | Expected Outcome |
|------------------------------|------------------|
| s1= "abcd",s2 = "abcd" | true |
| s1= "",s2 = "" | true |
| s1= "abcd",s2 = "" | false |
| s1= "",s2 = "abcd" | true |
| s1 = "aef",s2 = "def" | false |
| s1 = "def",s2 = "deg" | false |
| s1 = "a",s2 = "att" | true |
| s1 = "poojan",s2 = "patel" | false |

## Program 6
### (a) All equivalent classes
| Class ID | Class |
|----------|-------|
| E1 | All sides are positive |
| E2 | two of its sides are zero |
| E3 | One of its sides are negative |
| E4 | Sum of two sides is less than third side |
| E5 | Any of the side/sides is negative |

### (b) Identify test cases to cover the identified equivalence classes. Also, explicitly mention which test case would cover which equivalence class.
| Test Case ID | Class ID | Test Case |
|--------------|----------|-----------|
| T1 | E1 | A = 1,B = 1,C = 1 |
| T2 | E1 | A = 3, B = 4, C= 5 |
| T3 | E2 | A = 0,B = 0,C = 1 |
| T4 | E3 | A = 0,B = 1,C = 2 |
| T5 | E4 | A = 1, B = 3, C = 8 |
| T6 | E5 | A = -1,C = 1,D = 5 |

### (c) For the boundary condition A + B > C case (scalene triangle), identify test cases to verify the boundary.<br/>
A = 1, B = 3, C = 2
### (d) For the boundary condition A = C case (isosceles triangle), identify test cases to verify the boundary.<br/>
A = 3,B = 2, C = 3
### (e) For the boundary condition A = B = C case (equilateral triangle), identify test cases to verify the boundary.<br/>
A = 30,B = 30,C = 30
### (f) For the boundary condition A2 + B2 = C2 case (right-angle triangle), identify test cases to verify the boundary. <br/>
A = 6,B = 8,C = 10
### (g)  For the non-triangle case, identify test cases to explore the boundary.
A = 20, B = 10,C = 5
### (h) For non-positive input, identify test points.
A = 0, B = 10, C = 0 <br/>
A = 0,B = 0,C = 0 <br/>
A = 0, B = -1, C = 10<br/>

# Section B
## (1) Control flow graph
![image](https://user-images.githubusercontent.com/83656790/231543244-da18f637-45c0-469d-a107-c8d8777d9c69.png)

## (2) Test Cases 
### (a) Statement coverage test set:  In this all the statements in code should be covered
<br/>

| Test Number | Test Case |
|-------------|-----------|
| 1 | Empty Vector  |
| 2 | Vector with one point |
| 3 | vector with two points with the same y component |
| 4 | vector with two points with different y components |
| 5 | vector with three or more points with different y components |
| 6 | vector with three or more points with same y components |

### (b) Branch Coverage test set:  In this all branch are taken atleast once
<br/>

| Test Number | Test Case |
|-------------|-----------|
| 1 | Empty Vector  |
| 2 | vector with one point |
| 3 | vector with two points with the same y component |
| 4 | vector with two points with different y components |
| 5 | vector with three or more points with different y components, and none of them have the same x component |
| 6 | vector with three or more points with the same y component, and some of them have the same x component |
| 7 |vector with three or more points with the same y component, and all of them have the same x component |

### (c) Basic condition coverage test set: Each boolean expression has been evaluated to both true and false

| Test Number | Test Case |
|-------------|-----------|
| 1 | Empty vector |
| 2 | vector with one point |
| 3 | vector with two points with the same y component, and the first point has a smaller x component |
| 4 | vector with two points with the same y component, and the second point has a smaller x component |
| 5 | vector with two points with different y components |
| 6 | vector with three or more points with different y components, and none of them have the same x component |
| 7 | vector with three or more points with the same y component, and some of them have the same x component |
| 8 | vector with three or more points with the same y component, and all of them have the same x component. |


