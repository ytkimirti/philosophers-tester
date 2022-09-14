# Philosophers Tester
A tester made for ecole42 project `philosophers`

It actually checks if philosophers wait correct amount of time
before sleeping or holds the forks.

## Usage
`python3 analyze.py count death_time sleep_time eat_time [eat_count]`

**NOTE:**
Executing the python file will attempt to execute the binary named ./philo
in the current directory.
	
You can also pipe the output of your philo command to this like shown.
`./philo 2 300 150 150 | python analyze.py 2 300 150 150`
