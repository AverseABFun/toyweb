# toyweb v0.1 spec

- runs over a TCP socket

## client format

values in square brackets[] are values that should be replaced
values in curly brackets{} are hex values
```
CLIENTtoyweb{0x702366}\n
tw:[path]\n
v[protocol version] [operation name]\n
[additional data]\n
\n
[body]
#CLIENTEND{0x702366};
```

## server format

values in square brackets[] are values that should be replaced
values in curly brackets{} are hex values
```
SERVERtoyweb{0x702366}\n
RTO: tw:[path]\n
v[protocol version] RTO: [operation name]\n
[additional data]\n
\n
[body]\n
#SERVEREND{0x702366};
```