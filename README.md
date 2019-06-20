## Overview
Simple Redis Proxy


## Usage

```
$ go build main.go

$ ./main

Redis Proxy
==============
password:   Password of the target redis server. ( Defaults to using `masterauth` )
hostname:   Hostname of the target redis server.
port:       Port of the target redis server.
cacert:     Path to the ca certificate ( Optional )


./main -hostname=<hostname> -port=<port> -cacert=<path-to-ca-cert> -password=<remote-redis-auth>

```

### Attaching Local Redis as a Slave
```
$ redis-cli slaveof localhost 5000 
```

### Issuing Commands


**Netcat**
```
nc localhost 5000
```

**Telnet**
```
telnet localhost 5000
```

### Redis Clients

Should be compatible with any functional redis client.
