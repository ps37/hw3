
command used to SSH to the remote server:
ssh -i key_pair_name1.pem ubuntu@52.0.179.30

key_pair_name1.pem is the key-vale pair generated during the creation of my server.

Following is the command used for makning a HTTP request using wget:
wget http://52.1.43.112/killer-whale-825-1920x1200.jpg

Following is the command used for making a HTTPS request using wget:
wget --ca-certificate /System/Library/OpenSSL/certs/52.1.43.112.crt https://52.1.43.112/killer-whale-825-1920x1200.jpg

Then a self signed certificate is generated using the following command:
sudo openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout /etc/apache2/ssl/apache.key -out /etc/apache2/ssl/apache.crt

This is the location of the self signed certificate on my local machine:
/System/Library/OpenSSL/certs/52.1.43.112.crt

A simple shell script "./scr.sh" is written to execute the above commands concurrently 20 times to lauch 20 concurrent clients to my server to download a ".jpg" image of 630KB in size.

The data rates and time taken for the downloads are noted down to make the analysis. 