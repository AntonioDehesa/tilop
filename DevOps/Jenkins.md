# Jenkins

## First contact
Today was my first contact with Jenkins.  
From the very little I could see today, Jenkins is a great CI tool, which, if used appropiately, can reduce the time to build, test, and develop software. 
My first approach was I need to integrate GitLab/GitHub with Jenkins. Although I have not been able to do so, I believe I am liking Jenkins, and i will get to fully grasp it. 

## Running Jenkins on Tomcat

### Mounting Jenkins on Tomcat
First of all, you must have Apache Tomcat up and running. After that, we can follow the next steps: 
1. Download the War file from the official Jenkins website. This can be done from [this link](https://www.jenkins.io/download/).
2. Copy the jenkins.war file to the subfolder *webapps* in the Tomcat installation folder. It will auto generate a jenkins folder.
3. Go to the URL in which your Tomcat is running. In my case, it is running on http://localhost:8079/jenkins. After deploying Tomcat for public access, this URL changed, but everything else is the same. 
4. After this, we will have to follow the Jenkins installation/configuration instructions. 

### Public access to Jenkins
To be able to access your Jenkins configuration from anywhere, there are a list of steps to follows. Not necessaryly in this specific order: 
1. Turn off Windows Firewall. Of course, this means that now, our system and server is vulnerable. But for now, this is *acceptable*. 
2. Port Forwarding: In your router, configure the port 80 (and 443 if you need HTTPS) to redirect to a specific port (in my case 8079) and to a specific IP. 
3. In the configuration files of Tomcat, you should write your corresponding port. 

With this, we should be able to access Jenkins *from anywhere*. I hope I did not miss any steps. 
**Remember: This is insecure. You still need to do some server-hardening. This are just the very basics. It is dangerous to leave it like this.**
