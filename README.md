collectl
========

Extending collectl to send process data to graphite

The idea is to use ```collectl --export graphite,192.168.1.113 -sZ``` and generate graphite metrics like:
```
process.<CMD>.<PID>.cpu
process.<CMD>.<PID>.sys
...
process.<CMD>.cpu
process.<CMD>.sys
...
```

Potential problems:
- what happen when the process is runned by an interpreter (python blabla, python bleble, aggregated together?? no!) 
- threads? 
- aggregate info in collectl or in graphite (aggregation-rules.conf) ?
- lot of data to send to graphite
- how do you choose which subset to send?
