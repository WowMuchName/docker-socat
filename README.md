# Alpine + Socat

Example redirecting the docker-socket onto the host-port 2222:

```sh
docker run -v /var/run/docker.sock:/docker.sock -p 127.0.0.1:2222:2222 -d wowmuchname/socat -d -d TCP4-LISTEN:2222,fork UNIX-CONNECT:/docker.sock
```
