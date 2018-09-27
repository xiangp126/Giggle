## nc
> nc | netcat | tcpdmp | ncat | socat

```bash
# dump bytes of 'tcpdump' to listening port of the remote machine
# server_ip = 10.124.10.102
tcpdump -i eth0 -s 0 -U -n -w - | nc -l server_ip 8080
```

> get the bytes from remote server and open them with wireshark

```bash
nc server_ip 8080 | wireshark -k -i -
```