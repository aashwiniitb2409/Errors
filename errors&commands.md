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
  
## Install WSL2  
['https://docs.microsoft.com/en-us/windows/wsl/install']  

## Install go on WSL2  
['https://ao.ms/how-to-install-golang-on-wsl-wsl2/']  
after adding environment variables in `.bashrc can be opened by vim .bashrc`. Run `source .bashrc`. And we are good to go (PUN NOT INTENDED) 


