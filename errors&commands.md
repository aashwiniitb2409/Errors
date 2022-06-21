# Errors I got during internship  

## SSL Certificate errors:  
  github.crt ssl certificate: `openssl s_client -showcerts -connect github.com:443 </dev/null 2>/dev/null|openssl x509 -outform PEM > /usr/local/share/ca-certificates/github.crt`  
  move it to: `/etc/ssl/certs`  
  then `sudo ca-update-certificates`  
  proxy.golang.crt ssl certificate: `openssl s_client -showcerts -connect proxy.golang.org:443 </dev/null 2>/dev/null|openssl x509 -outform PEM > /usr/local/share/ca-certificates/proxy.golang.crt`  
  move it to: `/etc/ssl/certs`  
  then `sudo ca-update-certificates`  
  


