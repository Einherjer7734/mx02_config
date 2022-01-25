


### Generate SSH Cert for TLS
```
openssl genrsa -out /etc/ssl/private/mx02.ipa.somberlain.eu.key 4096
Generating RSA private key, 4096 bit long modulus
...........................................................++++
.........................................................................................................................................................................++++
e is 65537 (0x10001)

openssl req -new -x509 -key /etc/ssl/private/mx02.ipa.somberlain.eu.key -out /etc/ssl/mx02.ipa.somberlain.eu.crt -days 365
You are about to be asked to enter information that will be incorporated
into your certificate request.
What you are about to enter is what is called a Distinguished Name or a DN.
There are quite a few fields but you can leave some blank
For some fields there will be a default value,
If you enter '.', the field will be left blank.
-----
Country Name (2 letter code) []:de
State or Province Name (full name) []:bw
Locality Name (eg, city) []:bi
Organization Name (eg, company) []:priv
Organizational Unit Name (eg, section) []:
Common Name (eg, fully qualified host name) []:mx02.ipa.somberlain.eu
Email Address []:

chmod 600 /etc/ssl/mx02.ipa.somberlain.eu.crt
chmod 600 /etc/ssl/private/mx02.ipa.somberlain.eu.key
```
