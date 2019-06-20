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

Once the connection becomes available you can do things like:

1. Attach your local Redis as a slave  
```
$ redis-cli slaveof localhost 5000 
```

2. Connect to the port to issue Redis commands against the master
```
nc localhost 5000

set hey there
```
