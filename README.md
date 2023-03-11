# Philosophers Tester

It's sometimes hard to spot errors in philosophers just by looking at the output. 

This simplifies the output a bit and checks for simple errors.

input:
```
0 1 has taken a fork
10 1 has taken a fork
11 1 is eating
11 1 is eating
100 1 is sleeping
```
output:
```
$ python3 ../../philosophers-tester/analyze.py 2 3000 150 150 <input
Reading lines from stdin
===== philosopher: 1 =====
has taken a fork
Wait 10ms
has taken a fork
Wait 1ms
is eating
is eating
Wait 89ms
	Philo should wait for at least 150ms before sleeping but it only waited for 89ms
is sleeping
** Encountered errors, exiting with 1 **
```




## Usage
`python3 analyze.py count death_time sleep_time eat_time [eat_count]`

By default it will execute the executable named `./philo` and use it's output.

```
$ python ./analyze.py 2 300 150 150
```

If you want, you can instead pipe the output

```
$ ./philo 2 300 150 150 | python ./analyze.py 2 300 150 150
```

