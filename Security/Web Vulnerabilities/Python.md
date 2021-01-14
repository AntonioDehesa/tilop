# OS Command Injection
## Problem statement: 
A security assessment in your organization recently identified an OS Command Injection exposure associated with the maintenance functionality of an application. The functionality in question allows for the testing of server network connections using the command "ping"; a command which is executed at the OS level using unvalidated user input. Your task is to appropriately remediate the injection vulnerability, and thus safeguard the application from compromise.
![1 - Formation](http://url/to/img.png)

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
![2 - Setup](http://url/to/img.png)

### Hack
This section is optional, but I highly encourage it. 
You get the opportunity to test the vulnerability on a live and responsive application. The laboratory gives you instructions on what to do, but it does not give you the exact attack commands. 
It is really useful, specially to see both the scope of the impact, as well as the easiness of the attack. 
![3 - Hack](http://url/to/img.png)

### Fix
Afterwards, we get the *Fix* section. In this section, our duty is to fix the vulnerable code. 
In this case, it was achieved by changing one line of code. Of course, in future labs it may be harder. 
First, the line of code that was changed:  
![4 - Fix A](http://url/to/img.png)  
Next, the new result now that the app has been fixed.  
![4 - Fix B](http://url/to/img.png)  

### Results
Finally, we get our score for the lab.  
![4 - Fix A](http://url/to/img.png)


### Source
* [SecureFlag](https://secureflag.owasp.org/)