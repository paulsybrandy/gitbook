# How to Kill a Port in Linux

```
netstat -tulnap        // list all ports and processes
netstat -anp|grep "port_number"     // show port details
sudo fuser -k Port_Number/tcp       // free the port needed

# or

lsof -n -i :'port-number' | grep LISTEN  // get port details
# sample response: java 4744 (PID) test 364u IP0 asdasdasda 0t0 TCP *:port-number (LISTEN)
kill -9 PID  // free port
```
