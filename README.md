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

See [here](https://git.uibk.ac.at/c7701188/meg_tutorials/-/tree/master/bash) for a very basic intro to bash. 

Further, you'll need to get used to working with a text editor. [Which](http://www.geekherocomic.com/comics-highres/2009-02-02-emacs-vs-vim.png) one you choose among the only two [serious options](https://linuxhint.com/vim_vs_emacs/) is up to you, of course.  


# -------------------

## General setup  

It might be beneficial to use ssh-keys instead of ssh-password. See this [quick guide](https://www.linuxbabe.com/linux-server/setup-passwordless-ssh-login) 



## Mount ZIDshare drive with [smbnetfs](https://manpages.ubuntu.com/manpages/trusty/man1/smbnetfs.1.html)  
(see also [here](https://www.uibk.ac.at/zid/anleitungen/laufwerkszugriff/netzlaufwerkverbindung-linux.html) for more info)  

```
mkdir ~/.smb; chmod 600 ~/.smb
echo 'auth "zidshare.uibk.ac.at" "UIBK/cxxxx" "yyyyyyy"' > ~/.smb/smbnetfs.conf
echo 'host zidshare.uibk.ac.at visible=true' >> ~/.smb/smbnetfs.conf
chmod 600 ~/.smb/smbnetfs.conf
mkdir ~/zidshare

# mount zidshare  

smbnetfs ~/zidshare
# the files should be in ~/zidshare/zidshare.uibk.ac.at/eutops/

# to unmount:
fusermount -u ~/zidshare 


## to get into the drive with smbclient (similar to ftp) (see [here](https://www.samba.org/samba/docs/current/man-html/smbclient.1.html)   
smbclient -U c7461138 -W UIBK //zidshare.uibk.ac.at/eutops
```





