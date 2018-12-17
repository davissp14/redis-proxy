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
cacert:     Path to the ca certificate.


./main -hostname=<hostname> -port=<port> -cacert=<path-to-ca-cert> -password=<remote-redis-auth>

```

Once a secure connection to the ICD Redis Server has been established, a slave can be attached by setting  
`slaveof 127.0.0.1 5000`
