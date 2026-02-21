# You Spin Me Round Robin

This program simulates Round Robin with different quantum length given a list of processes with arrival and burst times. 

Processes that arrive at time t are added to the queue before the process ending at t-1 is added back to the queue.

## Building
To build, run
```shell
make
```

## Running
Run
```shell
./rr [input file] [quantum length]
```

The input file should be in the format:
```
n
pid_1, arrival time, burst time
...
pid_n, arrival time, burst time
```
where n is the number of processes in the list.

### Results
Example file processes.txt is below.
```
4
1, 0, 7
2, 2, 4
3, 4, 1
4, 5, 4
```

Example results are below.
```shell
$ ./rr processes.txt 2
Average waiting time: 5.00
Average response time: 1.50
```

## Cleaning up

To clean up, run
```shell
make clean
```
