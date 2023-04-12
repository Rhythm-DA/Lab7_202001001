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


