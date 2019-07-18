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


$ ./main -hostname=<hostname> -port=<port> -cacert=<path-to-ca-cert> -password=<remote-redis-auth>

Secure connection is now available on port `5000`

```

The Proxy connection will bind to port 5000 and once it has indicated that the connection is available you should be good to go. 


### Redis Cli
```
redis-cli localhost 5000
```


### Redis Clients

Should be compatible with any functional redis client.
