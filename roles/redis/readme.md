#Redis

## Monitoring

####Availability
The redis server will respond to the PING command when running properly

```
$ redis-cli -p 6380 -h redis.example.com -p 6379 PING
PONG
```

####Memory usage
Since we generally recommend setting the maxmemory size, it is possible to calculate the percentage of memory in use and alert based on result
```
$ redis-cli -p 6380 INFO |grep used_memory:
used_memory:424992
$ redis-cli config get maxmemory
1) "maxmemory"
2) "10000000"
```

####Uptime
Alert if uptime is less than you expect
```
$ redis-cli -p 6380 INFO |grep uptime_in_seconds
uptime_in_seconds:86514
```

## Statistics

####Cache hit rate
This information can be calculated from the INFO command
```
$ redis-cli -p 6380 INFO stats |grep keyspace
keyspace_hits:1920
keyspace_misses:930
```
Key eviction and expiration
Eviction occurs when redis has reached its maximum memory and maxmemory-policy in redis.conf is set to something other than volatile-lru.
```
$ redis-cli -p 6380 INFO stats |grep evicted_keys
evicted_keys:11582
```
Keys in redis can be set with a time to live which is generally a good practice
```
$ redis-cli -p 6380 SET mykey myvalue EX 600
```
It is a good idea to keep an eye on the expirations to make sure redis is performing as expected
```
$ redis-cli -p 6380 INFO stats |grep expired_keys
expired_keys:15436
```

####Key Space
We also recommend graphing the size of the keyspace as a quick drop or spike in the number of keys is a good indicator of issues.
```
$ redis-cli -p 6380 INFO keyspace
```
#### Keyspace
db0:keys=1075,expires=1075,avg_ttl=2110
Workload statistics
The final two stats that we recommend graphing are the following that indicate the workload place on the redis server
```
$ ~/tmp/redis-2.8.17/src/redis-cli INFO stats |egrep "^total_"
total_connections_received:70725
total_commands_processed:70723
```

###Redis high traffic connection issue
echo 1 > /proc/sys/net/ipv4/tcp_tw_reuse
echo 1 > /proc/sys/net/ipv4/tcp_tw_recycle


###Ref:
1. http://redis4you.com/articles.php?id=014&name=redis
2. http://redis4you.com/articles.php?id=012&name=redis
3. http://download.redis.io/redis-stable/redis.conf
4. http://shokunin.co/blog/2014/11/11/operational_redis.html