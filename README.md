# openresty-nginx-mail-proxy
Using openresty(1.15.8.1) or nginx as a mail proxy. Add  and change some function that initial nginx functions not so well or not as we expected.

# Steps
1. Download openresty directory.

2. Compile and build openresty.

   ./configure --prefix=/home/openresty/ --with-pcre-jit --with-mail --with-mail_ssl_module
   
   make
   
   make install

3. Copy the nginx.conf into your working directory and replace it with the old nginx.conf.

   Add the mail servers that you want to be proxyed in nginx.conf file.

4. Configure your mail client, set the proxy Server(ie, the openresty/nginx server).

   For Foxmail as example:
   
   Type: POP3
   
   Account: your_email@github.com
   
   Incomming: 192.168.10.1(change it to your openresty server ip)   SSL:(optional)  Port: 110/995(Your openresty Listening port)
   
   Outcoming: 192.168.10.1(change it to your openresty server ip)   SSL:(optional)  Port: 25/465(Your openresty Listening port)

5.Now you can send/recv emails.

