# rancher-agent-sni

This is a Rancher Agent Docker image that thas the Python OpenSSL library installed.  This is to allow the use of an SSL certificate that uses a Subject-Alternative-Name of the IP address in addition to the hostname.

Without this library, the agent will return the following error when trying to register.
 `requests.exceptions.SSLError: hostname '10.102.50.12' doesn't match either of 'rancher.mydomain.local', '10.102.50.12'` 
 
[https://github.com/rancher/rancher/issues/8792](https://github.com/rancher/rancher/issues/8792)