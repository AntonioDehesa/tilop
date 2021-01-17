# Burp Suite: Introduction
## Container

After downloading Burp Suite, we need a target. For this, we will use DVWA (Damn Vulnerable Web Application).  
We could use it with Apache, but it would be easier to simply use a container. For this, we have to pull the container and initialize it. 
These are the commands: 

The ran instructions, in different terminals, where: 
```bash
docker pull vulnerables/web-dvwa
docker run --rm -it -p 80:80 vulnerables/web-dvwa
```
## First request

We have to use Burp Suite as a proxy with our browser (in this case, Firefox).
When we send a request, Burp Suite intercepts it. It will show us information about it, such as: 
* Method
* Host
* User-Agent, which can be modified to *trick* the page into thinking we are using another browser or device
* Accept
* Accept-language
* Accept-Encoding
* Connection
* Referer
* Cookie
* Upgrade-Insecure-Requests
![Burp suite: First Request](https://github.com/AntonioDehesa/tilop/blob/main/Images/Security/PenTest/BurpSuite/Introduction/2%20-%20First%20Request.png)

## After forward
As it is a proxy, we intercept the request, and we can forward it afterwards. Once we do this, the request is fulfilled. 
![Burp suite: After Forward](https://github.com/AntonioDehesa/tilop/blob/main/Images/Security/PenTest/BurpSuite/Introduction/3%20-%20After%20Forward.png)

## Options
If we select a line of the request and right click it, it shows us a lot of options. 
We will select "Change Request Method"

![Burp suite: Options](https://github.com/AntonioDehesa/tilop/blob/main/Images/Security/PenTest/BurpSuite/Introduction/4%20-%20Options)

## Change Request Method

With this option, we can change the Get Request into a Post Request. This is only an example of what we can do with Burp Suite. 

![Burp suite: Change Request Method](https://github.com/AntonioDehesa/tilop/blob/main/Images/Security/PenTest/BurpSuite/Introduction/5%20-%20Change%20Request%20Method.png)

## Repeater

This option allows us to get the same request we just did, but changing the parameters. It is really useful for testing different payloads, and seeing the results in plain text. 

![Burp suite: Repeater](https://github.com/AntonioDehesa/tilop/blob/main/Images/Security/PenTest/BurpSuite/Introduction/7%20-%20Repeater.png)


## Compare

This option allows us to compare different results of the payloads.

![Burp suite: Compare](https://github.com/AntonioDehesa/tilop/blob/main/Images/Security/PenTest/BurpSuite/Introduction/8%20-%20Comparer.png)


## Result of a succesful payload
Here we can see the results of a succesful payload.

![Burp suite: Succesful payload](https://github.com/AntonioDehesa/tilop/blob/main/Images/Security/PenTest/BurpSuite/Introduction/11%20-%20Correct%20Payload.png)
