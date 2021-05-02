#Hero CTF
## PwnQL #1

Category | Points 
--- | --- 
Web | 50

- Look at the source code of the page, we can see:
```
<! - Hello dev, do not forget to remove login.php.bak before committing your code. ->
```
- Go to chall1.heroctf.fr:8080/login.php.bak, download the file
- See password LIKE: password
- Enter the login = admin and password = %
- Get the flag

### Flag=Hero{pwnQL_b4sic_0ne_129835}