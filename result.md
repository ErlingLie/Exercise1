# Results of concurrency test


When running the program described in this exercise we get different outputs each time. One would expect to get 0, as we increment and decrement exactly 1 000 000 each. However this is not the case in practice.

I got results such as 
''' 
erlingsl@Erlings-PC:~/ttk4145/Exercise1/go$ go run foo.go
The magic number is: 48066
erlingsl@Erlings-PC:~/ttk4145/Exercise1/go$ go run foo.go
The magic number is: 19762
erlingsl@Erlings-PC:~/ttk4145/Exercise1/go$ go run foo.go
The magic number is: -17332
erlingsl@Erlings-PC:~/ttk4145/Exercise1/go$ go run foo.go
The magic number is: 20901
'''

The reason for this is best described with an example.

1. The incrementor reads the value of *i* which is 0.
2. The thread switches and the decrementor reads the value of *i* to be 0.
2. The thread switches and the incrementor writes its result *1* to i.
3. The thread switches and the decrementor writes its result *-1* to i.

In this example the incrementor and decrementor changed the value of *i* exactly once each, but nevertheless *i* ended up as -1.

When we increment and decrement a million times this scenario will happen multiple times, resulting in a result different from 0.