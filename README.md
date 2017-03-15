# SSL-Certificate
Simplified Certificate generation for (Local Blyk Server)

I created this simple way for creating SSL certificates for loacl blynk server and other applications
who require customs SSL Certificates.

 Commands for generating ssl certificates are available at https://github.com/blynkkk/blynk-server#blynk-server

******************************************************************************************************************************************
* For simplicity Blynk already provides server jar with built in SSL certificates, so you have working server out of the box via SSL/TLS *
* sockets. But as certificate and it's private key are in public this is totally not secure. So in order to fix that you need to provide *
* your own certificates. And change below properties with path to your cert. and private key and it's password. See how to generate self-*
* signed certificates here                                                                                                               *
*                                                                                                                                        *
*  #points to cert and key that placed in same folder as running jar.                                                                    *
*                                                                                                                                        *
* server.ssl.cert=./server_embedded.crt                                                                                                  *
* server.ssl.key=./server_embedded.pem                                                                                                   *
* server.ssl.key.pass=pupkin123                                                                                                          *
******************************************************************************************************************************************
* https://github.com/blynkkk/blynk-server#blynk-server
* Generate own SSL certificates
* Generate self-signed certificate and key
* openssl req -x509 -nodes -days 1825 -newkey rsa:2048 -keyout server.key -out server.crt
* Convert server.key to PKCS#8 private key file in PEM format
* openssl pkcs8 -topk8 -inform PEM -outform PEM -in server.key -out server.pem
*   
In this way i have extracted the commands https://github.com/blynkkk/blynk-server#blynk-server and comfile it to executble 
for windows ".exe" the Certificate generated will be valid for 3 years or 1095 days.
the exe file will create new folder known as Cert\Client\Blynk.cert,Blynk.key and Cert\Server\Blynk.cert,Blynk.key
any comments please post at community.blynk.cc
