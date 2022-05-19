# Self Signed Certificate For Android
General，java application use `jks` keystore store certificate. But android don't support `jks` keystore. You need convert `jks` keystore to `bks`.

## Dependences
Install `openssl`,`keytool`,[JDK 1.8](https://www.myfreax.com/tag/java/) in your computer.

## Create Self Signed Certificate
```shell
./mkcert.sh
```

```
Generating RSA private key, 2048 bit long modulus (2 primes)
.....................................................................................................................................................................................+++++
...............+++++
e is 65537 (0x010001)
You are about to be asked to enter information that will be incorporated
into your certificate request.
What you are about to enter is what is called a Distinguished Name or a DN.
There are quite a few fields but you can leave some blank
For some fields there will be a default value,
If you enter '.', the field will be left blank.
-----
Country Name (2 letter code) [AU]:  
State or Province Name (full name) [Some-State]:
Locality Name (eg, city) []:
Organization Name (eg, company) [Internet Widgits Pty Ltd]:
Organizational Unit Name (eg, section) []:
Common Name (e.g. server FQDN or YOUR name) []:
Email Address []:
Please Enter Keystore Alias Name? myfreax.com 
Please Enter Keystore Password? myfreax.com
Importing keystore keystore.p12 to keystore.bks...
```
## You can find bellow files in current directory
```
bcprov.jar  fullchain.pem  keystore.bks  mkcert.sh  privkey.pem  README.md
```