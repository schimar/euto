# euto ws 

## login  

In order to log into the ws, you need to log into the UIBK VPN as well as https://fwauth-ext.uibk.ac.at. Then, you can log in to euto with your username and password:  

```
ssh <user>@lt181-eutops.uibk.ac.at
```

NOTE: it is useful to supply the following option when ssh'ing. This will help keep the connection alive for longer:

```
ssh -o ServerAliveInterval=300

# this can also be changed in your .bashrc, i.e. set an alias:
alias ssh='ssh -o ServerAliveInterval=300'  

``` 

See [here](https://git.uibk.ac.at/c7701188/meg_tutorials/-/tree/master/bash) for a very basic intro to bash. You'll need to get used to working with a text editor. [Which](http://www.geekherocomic.com/comics-highres/2009-02-02-emacs-vs-vim.png) one you choose (among the two only serious options) is up to you, of course.  


## Advanced usage

snakemake 

tmux 


