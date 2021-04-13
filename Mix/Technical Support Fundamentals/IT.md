# What is ITThanks to IT, we can communicate massive amounts of information immediately, all across the world. But what is it? 
IT, or Information Technology, is the use of digital technology, like computers and internet, to store and process data into useful information. The industry recognizes as IT to the jobs and resources related to computing technologies. 
But IT is not just about the jobs and resources, but also about the people working in it. 
* What good is technology if no one can use it

## What do Technical Support Specialists do
An IT support specialist makes sure that an organization's technological equipment is running smoothly. This includes managing, installing, maintaining, troubleshooting and configuring office and computing equipment.

## History of Computing
A computer is a device that stores and processes data by performing calculations. 
Before we had actual computer devices, the term computer was used to refer to someone who actually did the calculation. 

Have you ever wondered why the alphabet isn't laid out in order on your keyboard? 
The keyboard layout that most of the world uses today is the qwerty layout, distinguished by the Q, W, E, R, T, and Y keys in the top row of the keyboard. 

There are many stories that claim to answer this question. Some say it was developed a slow down typist so they wouldn't jam old mechanical typewriters. 
Others claim it was meant to resolve problem for telegraph operators. One thing is for sure, the keyboard layout that millions of people use today isn't the most effective one. 
Different keyboard layouts have even been created to try and make typing more efficient. 
Now that we're starting to live in a mobile-centric world with our smartphones, the landscape for keyboards may change completely. 
My typing fingers are crossed. In the technology industry, having a little context can go a long way to making sense of the concepts you'll encounter. 

## History of the computer
* First, data storage started with punch cards
* Afterwards, we moved on to magnetic tape


## Character encoding 
It is used to assign binary values to characters, so humans can read them. 
Almost like a dictionary. 
The oldest encoding standard is ASCII. 
The first ASCII character is a, represented as 01100001 in binary. It was good, but eventually, we needed more. 
Today, we use UTF 8. It even allows us to represent emojis. 

## Abstraction 

When using our computers, we don’t interact with it using ones and zeros. We don’t send 1 and 0 through our mouse, and we don’t send the specific ones and zeros with our keyboard to represent characters. 
We just use them, and they do it for us. This is called abstraction. 
It hides complexity by providing a common interface. 


## Computer architecture overview 

The four main layers of a computer are: hardware, software, operating system, and the users. 


# The Modern Computer

## Ports 
Connection points that we can connect devices to that extend the functionality of our computer. 

## CPU

The brain of the computer. It does all the calculations and data processing. 

The CPU uses a transition book to translate and perform functions on our data. This transition book is called an instruction set, which is literally just a list of instructions that our CPU is able to run. Functions like adding, subtracting, copying data are all instructions that our CPU can carry out. Every single program on your computer, while extremely complex, is broken down into very small and simple instructions found in our instruction set. Instruction sets are hard-coded into our CPU. So different CPU manufacturers may use different instructions sets. But they generally perform the same functions. It's like how car manufacturers build their engines differently but they all get the same job done. 

## RAM (Random Access Memory)

Stores data temporarily. Our programs, and data that our CPU will use immediately are stored here, so it has a faster access to it. 

Stores data that we want to access quickly. But the RAM does not store this data permanently. 
To run a program, we need to copy it to the RAM, as well as the data we are going to use with it. 
The most commonly type of RAM in a computer is D-RAM. Dynamic random-access memory. 
Ones and zeros are stored in microscopic capacitors. 
This is either the charge or discharge represented by one or zero. These semiconductors are put into chips that are on the RAM and store our data. There are also different types of memory states that DRAM chips can be put on. The more modern DIMM sticks, which usually stands for Dual Inline Memory Module, have different sizes of pins on them. I should call out, we don't really buy RAM based on the number of DRAM chips they have. They are labeled by the capacity of RAM on a stake, like an 8 gig stick of RAM. After DRAM was created, RAM manufacturers build something called SDRAM which stands for Synchronous DRAM. This type of RAM is synchronized to our systems' clock speed allowing quicker processing of data. In today's system, we use another type of RAM, called double data rate SDRAM, or DDR SDRAM for short. Most people refer to this RAM as DDR, even shorter. There were lots of iterations of DDR, from DDR1, DDR2, DDR3 and now, DDR4. DDR is faster, takes up less power, and has a larger capacity than earlier SDRAM versions. The latest version, DDR4, is the fastest type of short term memory currently available for your computer. And faster RAM means that programs can be run faster and that more programs can run at the same time. Keep in mind that any RAM sticks you use need a compatible motherboard with a different number of pins aligned with the motherboard RAM slots. Just like with the CPU, make sure that your motherboard is compatible with any RAM sticks that you buy. Up next, we'll take a deep dive into motherboards.

## Hard Drive

Holds all the data. 

## Programs

Basic instructions that tell the computer what to do. 


## External Data Bus

Row of wires that interconnect the parts of our computer. 


## Registers 

Components inside the CPU, which store the data that our CPU works with. They are like workspaces. 

## MCC

Memory Controller Chip. Bridge between the CPU and the RAM. 
When the CPU needs information from the RAM, it tells the MCC. The MCC then looks for the information in the RAM, and once it finds it, it sends it through the EDB. 
This is done through the Address Bus. It connects the CPU to the MCC and sends over the locations of the data in the RAM. 

## Cache

Faster than the RAM. Smaller than the RAM, but it stores data that we use often, and lets us quickly reference it. 
There are three different levels of cache: 
* L1
* L2
* L3
L1 is the fastest, but the smallest cache. 

## Clock wire

Our CPU has an internal clock that keeps its operational in sync. It connects to the clock wire. 
When you send or receive data, it sends a voltage to the clock wire, referred as the clock cycle. 


## Motherboard. 

The circuit board that connects all your components together. 
You can't just buy a bunch of parts and expect them to work together. There are different ways CPUs fit on motherboards using different sockets. Your CPU might have lots of tiny pins that either stick out or have contact points that look like dots. Depending on your motherboard, you need to make sure these CPUs fit correctly in the socket. 
There are currently two major types of CPU sockets: 
* Land Grid Array also known as LGA
* Pin Grid Array, also known as PGA. 
In an LGA socket there are pins that stick out of the motherboard. The socket size may vary. So always make sure you CPU and socket are compatible beforehand. 
The other type of socket is the PGA socket, where the pins are located on the processor itself. 
If you purchase a CPU, you'll see that it has either a 32 bit or 64 bit architecture. What does that mean? Well, we know we can process 8 bits in binary. Now, imagine how we can process with 32 or even 64 bits. CPUs that have 32 bit or 64 bit architecture are just specifying how much data it can efficiently handle. You can read more about the differences between 32 bit and 64 bit architecture in the next reading. For now, the main takeaway is that the CPU is one of the most important parts of a computer. So we have to make sure it's compatible with all other components and can perform well for our computing needs.

It has the chipset, which decides how components talk to each other. 
The chipsets are made of two chips: 
* Northbridge: interconnects stuff like RAM and video cards 
* Southbridge: maintains our IO controllers, like hard drives, usb devices, etc. 
In some modern CPUs, the northbridge is integrated in them. 
Form factor in a motherboard is the size. There´s ATX, ITX, mini ITX, nano ITX and pico ITX. 


## Drivers 

The drivers contain the instructions the CPU needs to understand external devices, like keyboards, usbs, etc. the CPU does not know that there is an external device to connect to, so it connects to the BIOS, or Basic Input Output Services. The BIOS is the one that initializes the hardware in our computer and gets the OS up and running. 
This BIOS is stored in the motherboard´s ROM, or Read-Only Memory.
The ROM is non-volatile. After the OS loads up, the ROM can then load non-essential drivers, from the hard drive. 
There is a new competitor for the BIOS: the UEFI. 
The UEFI stands for Unified Extensible Firmware Interface. It performs the same functions, but better. Better compatibility and support. 
Sometimes, computers run a test to check if the hardware is ok. This is called a Power On Self-Test or POST.  
To save the settings for the BIOS, there is a special chip called the CMOS. 


# Software

## SSH 
Secure Shell is a protocol implemented by other programs to securely access one computer from another. To use it, you need a SSH client in the computer that you are using to connect to another computer, and a SSH server in the computer you are trying to connect to. 
On the remote computer, the server is a process that is constantly running, scanning for an incoming connection. 
For Linux, the most popular SSH is OpenSSH. For windows, it is Putty. 
We need: 
* An account in the host 
* The hostname or the IP address of the host
Now that we are connected, everything we type, is sent through secure channels. 
We can authenticate using a password, but this is not super secure. It is better to use an authentication key. 
Private and public keys. 

## VPN 
Virtual Private Network. 
Another way to connect securely remotely. 
 
The default port for SSH is 22. 


It is the Remote Desktop Protocol, or RDP. This protocol is available for Linux and Mac. 


# Components of an OS

The OS is the whole package that manages computers resources and lets us interact with it. There are two main parts to an OS: 
* Kernel
* User space
The kernel is the main core of an OS. It talks directly to the hardware and manages our systems resources. The users do not interact directly with it. We interact with the user space. Which means, everything outside the kernel. 

The kernel does file storage in file management. 
Besides, with the kernel´s process management, we manage the order the programs run in, how many resources they take up, how long they run, etc. 
Memory management: the kernel optimizes memory usage and make our applications have enough memory to run. 
Finally, the kernel manages IO. 

## File and files systems 

There are three main components to handling files on an OS: 
* The file data
* Metadata
* File system 

## File System 

There are a lot of file systems, and the OS needs to know which one it is using. 
They operate at different speeds, some support the storage of large amounts of data, others not large amounts of data, etc. for example, windows uses NTFS, MacOS uses HFS+, and linux uses whatever every distribution wants, but an unofficial standard is ext4. 

Data is stored in blocks. It does not always sit in one piece. It is divided in blocks, as to not leave empty spaces. 

Metadata is the file that tells when it was created, who modified it, when, etc. 



## Process management 

Processes are programs executing. Programs are applications you can run. 
The difference is, there can be many processes for one program. 
As there are finite resources in a computer, we need the kernel to manage the resources to run the programs, so we can run as many programs as possible. 
For example, the CPU. There is only one CPU, yet we have to run several processes at the same time. How does this happen? Time slices. Time slice is a very short interval in which a process can act. After that, its another´s processes turn to act. 


## Memory management 

Virtual memory: combination of hard disk and RAM. When we execute a process, we take the data of the program in chunks we call pages. We store these pages in virtual memory. If we want to read and execute these pages, they have to be sent to physical memory or RAM.
We could store the entire program in the RAM, if the RAM could hold it. 
Of course, the kernel does not load the entire application in the RAM. Just the parts we would normally need. If we go to an obscure menu in the app, it could take a little longer to load, and freeze, because it would need to load it from virtual memory, to RAM. 
IO management 

The kernel manages the peripherals, the data transfer between these, etc. 


## User space

This is where the users usually interact. 
The CLI, GUI and whatever the user does is in here. 


## The boot process 

First, the computer is powered on. Then, the BIOS/UEFI runs the POST. 
After that, a boot process will be chosen. Then, the OS will start loading. 
Then, drivers are loaded. Then, essential system processes. 

# Networking

The Internet is just an interconnection of computers around the world, like a giant spider web that brings all of us together. We call the interconnection of computers a network. Computers in a network can talk to each other and send data to one another. 
The simplest of networks would be two computers communicating. 
We could communicate several computers or machines to one network. That network, and another network together and form a new, bigger network. The size of a city block. 
Several blocks to form a city-wide network. 
Several cities to form a bigger network, and so on and so forth. 
The internet is basically lots of networks communicating. 

But don't make the mistake of thinking the Internet is the World Wide Web. The Internet is the physical connection of computers and wires around the world. 
The Web is the information on the Internet. We use it to access the Internet. 
The World Wide Web isn't the only way we can access the Internet. Your e-mail, chat, and file-sharing programs are also ways you can access the Internet. 
The Internet is composed of a massive network of satellites, cellular networks, and physical cables buried beneath the ground. We don't actually connect to the Internet directly. Instead, computers called servers connect directly to the Internet. Servers store the websites that we use, like Wikipedia, Google, Reddit, and BBC. These websites serve content. The machines that we use, like our mobile phones, laptops, video game, consoles and more, are called clients. 
Clients request the content, like pictures, websites, from the servers. Clients don't connect directly to the Internet. Instead, they connect to a network run by an Internet service provider or ISP. 
ISPs have already built networks and run all the necessary physical cabling that connects millions of computers together in one network. They also connect to other networks and other ISPs. 
But how do the clients know how to get to servers? 
Computers on a network have an identifier called an IP address. An IP address is composed of digits and numbers like 100.1.4.3. 
Devices that can connect to a network have another unique identifier called a MAC address. MAC addresses are generally permanent and hard-coded onto a device. 
When you send or receive data through a network, you need to have both an IP and a MAC address. 
An IP address is your house address, while the MAC address is the name of this recipient of the letter. 
One thing to call out is that data that is sent through a network is sent through packets. There are little bits of data, and you guessed it, ones and zeros. 
When we move data through the network, we break them down into packets. When a packet gets to its destination, it will rearrange itself back in order. 

## How they connect 

* Ethernet cable: physically connects to the network through a cable. 
* Wifi: Wireless networking. We connect using radio signals and antennas. 
* Fiber optics: the cables contain glass fibers that move light instead of electricity. The zeros and ones get sent through a beam of light.
All these is to connect to the router. Several computers connect to the router, and it connects to the rest of the internet. 
The packets of information get sent from one computer to the router, then to another computer. 
If we want to sent info to a computer in another network, it would be like this: 
Computer A wants to send something. It sends it to the router. The router connects to the ISP, which looks for the router of the recipient computer, then sends the info to that router, and that router connects to computer B. 



# Networking protocols

Set of rules that make sure the packets of data that we sent and receive are routed efficiently, are not corrupted, are secure, go to the right machine, and are named appropriately. 

The main protocols that will be covered in this course, are TCP and IP. 
* TCP: Transmission Control Protocol: handles reliable delivery of information from one network to another. It was an important part of the creation of the internet since it lets us share information with other computers. 
* IP: Internet Protocol: responsible for delivering the packets to the right computers. 

## The Web 

The web is the most common way we can use the internet. We can access websites through the web. And websites are basically documents formatted with HTML, stylized with CSS, and that act with JavaScript files. 
We can access a website using an URL, or Universal Resource Locator. 
Example of an URL: www.example.com

The www part means World Wide Web
Then, it comes the domain name. this would be, example. 
The last part is the domain ending or protocol. This shows us a little about the purpose of the site.

IP has several versions. The currently used protocol is IPv4, which is an address of 32 bits, divided in 4 groups. This gives us over 4.3 billion possible ip addresses. But, these are not enough. 
Then, there is IPv6. 128 bits. With this, we have 2 to the 128 possible addresses. 

NAT: Network Address Translation. This lets organizations use one public IP, but several internal, private Ips. 


Internet of Things or IoT

It is the idea that more and more devices are connecting to the internet, even if not necessarily, like smart showers. 



# Software 

## Types of software 

Application software: software created to fulfill a specific need. 
System software: software used to keep our core system running, like operating system tools or utilities. 

Firmware: a type of system software. It is permanently stored on a computer component, like the BIOS. 


Compiled programming languages: they use human readable instructions, and then they are compiled, and translated to binary code. 
Interpreted programming languages: these are not compiled, but only interpreted. 
A file for an interpreted programming language is a script. 



## Resources 
* [Coursera - Google: Technical Support Fundamentals](https://www.coursera.org/learn/technical-support-fundamentals)