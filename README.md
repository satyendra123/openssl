# openssl
i want to generate the csr and pem key file. this is the command i have used for generating the ssl certificate


step-1) download the openssl https://sourceforge.net/projects/openssl/   

step-2) when i open it then go to bin folder and again go to inside the folder we have the .exe file and openssl.cnf file. by double click into the .exe file my openssl is opened. but at the above it is displaying that C/program files/OPENSSL/openssl.cnf file file is not present. so what i do is open the environment variable and click on the New it will ask the variable name and variable value. in the variable name write the OPENSSL_CONF and in the variable value write the C:\Users\Satyendra Singh\Downloads\openssl-1.0.2j-fips-x86_64\OpenSSL\bin\openssl.cnf then click on ok. and again open the openssl.exe and it will not ask for the openssl.cnf file is not found. now it will work. just paste the command below and it will generate the certificate.csr file and private.key file

Steps to Set the OPENSSL_CONF Environment Variable:
Find the Full Path to openssl.cnf Your openssl.cnf file is located at:
C:\Users\Satyendra Singh\Downloads\openssl-1.0.2j-fips-x86_64\OpenSSL\bin\openssl.cnf

Set the OPENSSL_CONF Environment Variable:

Open System Properties by pressing Win + R, then typing sysdm.cpl and pressing Enter.
Go to the Advanced tab and click on Environment Variables.
Under the System variables section, click New.
For Variable name, enter OPENSSL_CONF.
For Variable value, enter the full path of your openssl.cnf file:




OpenSSL> req -newkey rsa:2048 -keyout private.key -out certificate.csr -days 365 -nodes
Generating a 2048 bit RSA private key
....................................................................+++
.......................................+++
writing new private key to 'private.key'
-----
You are about to be asked to enter information that will be incorporated
into your certificate request.
What you are about to enter is what is called a Distinguished Name or a DN.
There are quite a few fields but you can leave some blank
For some fields there will be a default value,
If you enter '.', the field will be left blank.
-----
Country Name (2 letter code) [AU]:IN
State or Province Name (full name) [Some-State]:UP
Locality Name (eg, city) []:NOIDA
Organization Name (eg, company) [Internet Widgits Pty Ltd]:housys
Organizational Unit Name (eg, section) []:houston
Common Name (e.g. server FQDN or YOUR name) []:skymark
Email Address []:singhsatyendra885@gmail.com

Please enter the following 'extra' attributes
to be sent with your certificate request
A challenge password []:
An optional company name []:
OpenSSL>
