# Errors I got during internship  

## SSL Certificate errors:  
  github.crt ssl certificate: `openssl s_client -showcerts -connect github.com:443 </dev/null 2>/dev/null|openssl x509 -outform PEM > /usr/local/share/ca-certificates/github.crt`  
  move it to: `/etc/ssl/certs`  
  then `sudo ca-update-certificates`  
  proxy.golang.crt ssl certificate: `openssl s_client -showcerts -connect proxy.golang.org:443 </dev/null 2>/dev/null|openssl x509 -outform PEM > /usr/local/share/ca-certificates/proxy.golang.crt`  
  move it to: `/etc/ssl/certs`  
  then `sudo ca-update-certificates`  
 
## To expose a service and run it through localhost:
  `kubectl port-forward service/nginx-service 8080:80`  
  where service = nginx-service running on port 80 can now be run with http://localhost:8080

## To uninstall golang
  `rm -rf /usr/local/go`
 
## To change go env variable
  `go env -w GOFLAGS=""`
  
## To uninstall WSL  
Just remove linux subsystem from the control panel  

## Install WSL2  
['https://docs.microsoft.com/en-us/windows/wsl/install']  

## Install go on WSL2  
['https://ao.ms/how-to-install-golang-on-wsl-wsl2/']  
after adding environment variables in `.bashrc can be opened by vim .bashrc`. Run `source .bashrc`. And we are good to go (PUN NOT INTENDED) 

## Install kubectl on WSL2  
['https://kubernetes.io/docs/tasks/tools/install-kubectl-linux/']  
**Problems with this documentation**:  
It says that kubectl latest version is `v1.24.2` but this version is faulty so download `v1.24.0`    

## Installing Kubebuilder
['https://book.kubebuilder.io/quick-start.html']  

## Install WSL REMOTE on VS CODE  
Downloading Remote WSL is easy on VS Code. There is an extension, we just have to install it.  

##  Downloading gcc executable file on WSL  
`apt-get install build-essential`  

## To know linux version and specifications  
`lsb_release -a`  

## To download postgresql on WSL  
`wget --quiet -O - https://www.postgresql.org/media/keys/ACCC4CF8.asc | sudo apt-key add -`  
`sudo sh -c 'echo "deb http://apt.postgresql.org/pub/repos/apt/ $(lsb_release -cs)-pgdg main" >> /etc/apt/sources.list.d/pgdg.list'`  
`sudo apt update`  
`sudo apt install postgresql postgresql-contrib`  

`service postgresql status`  
**Running Postgres:** `sudo su postgres`  
`psql`  
**Check Version:** `SELECT version();`  


