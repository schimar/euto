# euto ws 

## Initial setup  

In order to log into the ws, you need to log into the UIBK VPN and log into https://fwauth-ext.uibk.ac.at. Then, you can log in to euto with your username and password:  

```
ssh <user>@lt181-eutops.uibk.ac.at
```

NOTE: it is useful to supply the following option when ssh'ing. This will help keep the connection alive for longer:

```
ssh -o ServerAliveInterval=300

# this can also be changed in your .bashrc, i.e. set an alias:
alias ssh='ssh -o ServerAliveInterval=300'  

``` 



