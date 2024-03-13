### This repository implement the better way to use concurrency in golang.This has two code `unfair` and `fair` way. In `unfair` way the task to each goroutines is not distributed uniformly. In `fair` way the task to each goroutines is distributed uniformly.
### I am writing code to calculate the total number of prime numbers from 1 - 100000000
## Output in unfair way

PS D:\golang\good-implementation-of-concurrency\unfair> go run main.go<br>
thread 0 [3, 10000003) completed in 55.3829514s<br>
thread 1 [10000003, 20000003) completed in 1m29.3189433s<br>
thread 2 [20000003, 30000003) completed in 1m48.8445482s<br>
thread 3 [30000003, 40000003) completed in 2m3.676358s<br>
thread 4 [40000003, 50000003) completed in 2m15.4956872s<br>
thread 5 [50000003, 60000003) completed in 2m18.7958588s<br>
thread 6 [60000003, 70000003) completed in 2m25.504147s<br>
thread 7 [70000003, 80000003) completed in 2m29.1626335s<br>
thread 8 [80000003, 90000003) completed in 2m34.1781205s<br>
thread 9 [90000003, 100000000) completed in 2m40.8713912s<br>
checking till 100000000 found 5761455 prime numbers. took 2m40.8719252s<br>

## Output of fair way

PS D:\golang\good-implementation-of-concurrency\fair> go run main.go<br>
thread 4 completed in 1m17.4563185s<br>
thread 9 completed in 1m17.632795s<br>
thread 0 completed in 1m17.632795s<br>
thread 2 completed in 1m17.3139058s<br>
thread 8 completed in 1m17.6315886s<br>
thread 6 completed in 1m17.632795s<br>
thread 7 completed in 1m17.632795s<br>
thread 3 completed in 1m17.6010472s<br>
thread 5 completed in 1m17.632795s<br>
thread 1 completed in 1m17.632795s<br>
checking till 100000000 found 5761455 prime numbers. took 1m17.632795s<br>
