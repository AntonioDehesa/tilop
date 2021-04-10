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
