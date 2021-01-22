# OS Command Injection
## Problem statement: 
A security assessment in your organization recently identified an OS Command Injection exposure associated with the maintenance functionality of an application. The functionality in question allows for the testing of server network connections using the command "ping"; a command which is executed at the OS level using unvalidated user input. Your task is to appropriately remediate the injection vulnerability, and thus safeguard the application from compromise.
![1 - Formation](https://github.com/AntonioDehesa/tilop/blob/main/Images/Security/Python/OS%20Command%20Injection/1%20-%20Information.JPG)

## Description of the vulnerability

OS Command Injection (aka Shell Injection) is a type of injection vulnerability that allows an attacker to input commands which are executed on the host operating system. 
This vulnerability is caused by insufficient input validation but are only possible if the web application accepts OS calls with user input. So, it is but a fail in application logic AND execution. 
This is different from Code Injection. In OS Command Injection, the attacker can input commands, which was the intended purpose, but there is not enough input validation. 
Code injection is when an attacker can input code into the web application, which was not the intended functionality. 
Code injection can lead to OS Command Injection, depending on the native language of the application. For example, in Python, we could do
```python
__import__(‘os’).popen(‘l’).read()
```
With this, we could see every file in the pwd. 

OS Command Injection is a language agnostic vulnerability. 

## Impact
The impact can go from *just* information leakage, such as getting the files in a folder, to the attacker obtaining total control on the system. 

## Example of attack
In the case that we have a web application that asks for a filename to compress said file, and the application does not validate the input, we could input 
```bash
Filename; rm -rf *.*
```
## Prevention

First, direct command input from the user should be avoided. 
If it is unavoidable, the input should be appropriately sanitized, and a whitelist should also be used whenever possible. 

## Lab

The SecureFlag labs are divided in three main sections:
* Setup
* Hack
* Fix

### Setup 
It is where you get your first contact with the web application of the problem. You see the code of the application (at least in this lab) and you can see the application running for the first time. After you have launched the application succesfully, you can get to the next section. 
![2 - Setup](https://github.com/AntonioDehesa/tilop/blob/main/Images/Security/Python/OS%20Command%20Injection/2%20-%20Setup.JPG)

### Hack
This section is optional, but I highly encourage it. 
You get the opportunity to test the vulnerability on a live and responsive application. The laboratory gives you instructions on what to do, but it does not give you the exact attack commands. 
It is really useful, specially to see both the scope of the impact, as well as the easiness of the attack. 
![3 - Hack](https://github.com/AntonioDehesa/tilop/blob/main/Images/Security/Python/OS%20Command%20Injection/3%20-%20Hack.JPG)

### Fix
Afterwards, we get the *Fix* section. In this section, our duty is to fix the vulnerable code. 
In this case, it was achieved by changing one line of code. Of course, in future labs it may be harder. 
First, the line of code that was changed:  
![4 - Fix A](https://github.com/AntonioDehesa/tilop/blob/main/Images/Security/Python/OS%20Command%20Injection/4%20-%20Fix%20a.JPG)  
Next, the new result now that the app has been fixed.  
![4 - Fix B](https://github.com/AntonioDehesa/tilop/blob/main/Images/Security/Python/OS%20Command%20Injection/4%20-%20Fix%20b.JPG)  

### Results
Finally, we get our score for the lab.  
![5 - Results](https://github.com/AntonioDehesa/tilop/blob/main/Images/Security/Python/OS%20Command%20Injection/5%20-%20Correct%20Answer.JPG)


### Source
* [SecureFlag](https://secureflag.owasp.org/)

# CSRF

## Description of the vulnerability

So, what is CSRF.  
CSRF is a type of attack where an authenticated user in a legitimate site clicks a link that takes them to an insecure webpage, that has a hidden POST form. This POST form uses the API of the legitimate site to make requests to the site using the legitimate users credentials. 

## Impact
The impact can go from *just* information leakage, to unwanted actions of the users, and possibly loss of users. 

## Example of attack
So, lets say there is a legitimate user that logged in to his bank account, called Bank.  
Now, this user clicks a link such as: www.insecureplace.com.  
Now, after clicking, we realizes nothing actually happens, so he closes that tab. After reloading his bank tab, he realizes that he lost some money. And this script is what happened. 
```html
<form action="http://bank.com/transfer.do" method="POST">

<input type="hidden" name="acct" value="MARIA"/>
<input type="hidden" name="amount" value="100000"/>
<input type="submit" value="View my pictures"/>

</form>
```
## Prevention

The prevention is quite easy, theoretically. By using a CSRF secret token, which will be hidden inside the site, and the server will be expecting this token with every POST, PUT, DELETE, etc, request. 
This Token should be completely random, as to ensure the security. 

## Lab

The SecureFlag labs are divided in three main sections:
* Setup
* Hack
* Fix

### Setup 
It is where you get your first contact with the web application of the problem.  
You see the code of the application (at least in this lab) and you can see the application running for the first time. After you have launched the application succesfully, you can get to the next section. 
![CSRF - Setup]()

### Hack
This section is optional, but I highly encourage it. 
You get the opportunity to test the vulnerability on a live and responsive application. The laboratory gives you instructions on what to do, but it does not give you the exact attack commands. 
It is really useful, specially to see both the scope of the impact, as well as the easiness of the attack. 
In this case, the legitimate user literally only has to click on a link, and if there is no CSRF token, thats it. 
![CSRF - Hack]()

### Fix
Afterwards, we get the *Fix* section. In this section, our duty is to fix the vulnerable code. 
In this case, it was achieved by adding three lines of code. It was quite simple, but it is a good example to show how easily we can make our app slightly more secure.  
![CSRF - Fix]()  
### Results
Finally, we get our score for the lab.  
![5 - Results](https://github.com/AntonioDehesa/tilop/blob/main/Images/Security/Python/OS%20Command%20Injection/5%20-%20Correct%20Answer.JPG)

# XSS

## Description of the vulnerability

So, what is XSS.  
XSS is a tpye of vulnerability that allows an attacker to introduce code in the application that was not supposed to be executed. There are three types of XSS: 
* Reflected: It immediately executes the injected code. 
* Stored: It stores the injected code, and every time that code gets called it gets executed.
* DOM: In here, the target of the attack is the environment of the app, so the client side code runs in an unnexpected way. The one that we will be seeing in this lab will be Reflected. 

## Impact
The impact can go from *just* information leakage, to basically anything, within the scopes of its own type of XSS. 

## Example of attack
If www.bank.com is vulnerable to XSS, we could do something like: 
```js
www.bank.com/<script>alert(1)</script>
```
This way, it will execute the code inside the script tag
## Prevention

In this lab, the way to solve it was really simple. We relied on codification of the special characters. 
Instead of <>, we would get &lt&mt of something like that. 
There are other ways to solve it, such as: 
* Whitelisting: We can use whitelisting to allow only certain words to be allowed. That would be ideal. 
* Sanitization: With this one, we encode the special characters such as <,>, (,), etc. Use with whitelisting, or in case you cant use whitelisting 
* Blacklisting: We forbid certain words. Last option, really. 

## Lab

The SecureFlag labs are divided in three main sections:
* Setup
* Hack
* Fix

### Setup 
It is where you get your first contact with the web application of the problem.  
You see the code of the application (at least in this lab) and you can see the application running for the first time. After you have launched the application succesfully, you can get to the next section. 
![CSRF - Setup]()

### Hack
This section is optional, but I highly encourage it. 
You get the opportunity to test the vulnerability on a live and responsive application. The laboratory gives you instructions on what to do, but it does not give you the exact attack commands. 
It is really useful, specially to see both the scope of the impact, as well as the easiness of the attack. 
As wee could see previously, we could just do 
```js
www.bank.com/<script>alert(1)</script>
```
![CSRF - Hack]()

### Fix
Afterwards, we get the *Fix* section. In this section, our duty is to fix the vulnerable code. 
In this case, the way to fix it was simply removing the *safe* tag. This would encode the output. We could also use a whitelist character per character, but this one is easier. 
![CSRF - Fix]()  
### Results
Finally, we get our score for the lab.  
![5 - Results](https://github.com/AntonioDehesa/tilop/blob/main/Images/Security/Python/OS%20Command%20Injection/5%20-%20Correct%20Answer.JPG)

