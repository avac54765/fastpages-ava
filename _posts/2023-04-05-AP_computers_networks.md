---
toc: true
comments: true
layout: post
title: Computers and Networks (Unit 4)
description: Add Definitions from Unit 4 Computer Systems and Networks
categories: [week 29]
---

## Requirements
> Work through College Board Unit 4... blog, add definitions, and pictures.  Be creative, for instance make a story of Computing and Networks that is related to your PBL experiences this year.


### How a Computer Works
> As we have learned, a computer needs aa program to do something smart.  The sequence of a program initiates a series of actions with the computers Central Processing Unit (CPU). This component is essentially a binary machine focussing on program instructions provided.  The CPU retrieives and stores the data it acts upon in Random Access Memory (RAM). Between the CPU, RAM, and Storage Devices a computer can work with many programs and large amounts of data.

List specification of your Computer, or Computers if working as Pair/Trio
- Processor GHz:  <mark>2.50 GHz</mark>
- Memory in GB:<mark> 8.0 GB </mark>
- Storage in GB: <mark>237 GB</mark>
- OS:  <mark>Windows Build 19044.2728 </mark>

Define or describe usage of Computer using Computer Programs. Pictures are preferred over a lot of text.  Use your experience.
- <mark>Input devices</mark>
    - includes: keyboards, microphones, cameras, mouses, scanners
    - where users input/interact with a computer
    - a hardware device that sends data to a computer, allowing you to interact with and control it

    ![image](https://user-images.githubusercontent.com/111486111/232163657-d90d1aeb-ee73-4967-bf27-5a9a0aa76ad2.png)

- <mark>Output devices</mark>
    - includes: monitors, printers, headphones, speakers, projectors, etc.
    - where users receive response from input action
    - a hardware device used to send data from a computer to another device or user

    ![image](https://user-images.githubusercontent.com/111486111/232163744-1d863e47-47d7-400a-8428-476785342d80.png)

![image](https://user-images.githubusercontent.com/111486111/232163417-7a72e15f-4f1c-4c6d-8f14-ccc66c4ec813.png)

- <mark>Program File</mark> = A file that contains instructions for the computer. The file is in a machine format that is ready to be executed directly by the computer.
    ![image](https://user-images.githubusercontent.com/111486111/232165519-4e959aa0-c699-4b66-bc4b-3508185f727a.png)
    We use program files everyday when constructing our projects. Markdowns and Notebooks are examples of program files.

- <mark>Program Code</mark> = computer code refers to the set of instructions, or a system of rules, written in a particular programming language
    ![image](https://user-images.githubusercontent.com/111486111/232166037-aab7fdb9-33fd-4518-a9c1-3df1774cc415.png)

    Program code is what goes inside our program files. Within these files are the actual pages/algorithms that we code/write.


- <mark>Processes</mark> = A process is an instance of a program running in a computer
    ![image](https://user-images.githubusercontent.com/111486111/232177774-b5e84d62-cbdc-4bed-9093-3fd03631af0a.png)

    Anytime we run our programs or algorithms, a process is running. We can have multiple processes running on one computer, which is called parallel processing. Currently, I have 7 apps running, 106 background processes, and 140 Windows processes running on my computer.


- <mark>Ports</mark>= A port is a virtual point where network connections start and end. Ports are software-based and managed by a computer's operating system. Each port is associated with a specific process or service.
    ![image](https://user-images.githubusercontent.com/111486111/232178015-de72c30d-6f6c-4db0-a4e8-f5c5a8b9e1f6.png)

    We used ports when deploying our projects on AWS. Every group needed to deploy using a different port number so that a user could be directed to the correct port/project when searching the project domain (if incorrect port= may be directed to wrong site).

- <mark>Data File</mark> = A data file is a computer file which stores data to be used by a computer application or system, including input and output data. A data file usually does not contain instructions or code to be executed (that is, a computer program).
    ![image](https://user-images.githubusercontent.com/111486111/232178179-674e4d1d-c201-4b2a-ac4a-8c6aa68c873c.png)

    We used data files when calling rest APIs from existing data sets in Trimester One. We also used data files when creating our databases. The database I created stored my data in a file in which I could access, add, and update data to.
 
- <mark>Inspect Running Code</mark>= With VScode, programmers are able to debug their code as it runs each step. This allows for programmers to see what each line is doing and where an issue may lie.
    ![image](https://user-images.githubusercontent.com/111486111/232178587-56069197-6297-4ba9-a636-2dbb218110b0.png)

    This was especially helpful to us when creating our databases.

- <mark>Inspect Variables</mark> = when debugging on vscode, you can see what variables are being created as you run your program. 
    ![image](https://user-images.githubusercontent.com/111486111/232179083-355c452b-fc29-404e-abf9-80be6fba379f.png)

    This was very useful when creating our databases. We were able to run our code and watch as new objects were being created and assigned.

![Computer Hardware]({{site.baseurl}}/images/cpu.jpeg)


### The Internet
> Watch/review College Board Daily Video for 4.1.1

- Essential Knowledge
    - <mark>A computing device</mark> is a physical artifact that can run a program. Some examples include computers, tablets, servers, routers, and smart sensors.
    - <mark>A computing system is a</mark> group of computing devices and programs working together for a common purpose.
    - <mark> A computer network</mark> is a group of interconnected computing devices capable of sending or receiving data.
    - <mark>A computer network</mark> is a type of computing system. 
    - <mark>A path</mark> between two computing devices on a computer network (a sender and a receiver) is a sequence of directly connected computing devices that begins at the sender and ends at the receiver.
    - <mark>Routing</mark> is the process of finding a path from sender to receiver.
    - <mark>The bandwidth </mark>of a computer network is the maximum amount of data that can be sent in a fixed amount of time.
    - Bandwidth is usually measured in bits per second

- Complete Vocabulary Matching Activity.  Incorporate this into your learnings from year.  To analyze measure path and latency use `traceroute` and `ping` commands from Linux Terminal.  
    - Path 
    - Route
    - Computer System
    - Computer Device
    - Bandwidth
    - Computer Network

> Watch/review College Board Daily Video 4.1.2

- Complete True of False Questions
![image](https://user-images.githubusercontent.com/111486111/232180994-871f8e2a-f119-4c9f-a444-6a00a3e98581.png)

- Essential Knowledge
    - The internet is a computer network consisting of interconnected networks that use standardized, open (nonproprierary) communication protocols.
    - Access to the internet depends on the ability to connect a computing device to an internet connected device.
    - A protocol is an agreed-upon set of rules that specify the behavior of a system.
    - The protocols used in the internet are open, which allows users to easily connect additional computing devices to the internet.
    - Routing on the internet is usually dynamic; it is not specified in advance
    - The scalability of a system is the capacity for the system to change in size and scale to meet new demands.
    - The internet was designed to be scalable
    - Information is passed through the internet as a data stream. Data streams contain chunks of data, which are encapsulated in packets. 
    - Packets contain a chunk of data and metadata used for routing the packet between the origin and the destination on the internet, as well as for data reassembly.
    - Packets may arrive at the destination in order, out of order, or not at all
    - IP, TCP and UDP are common protocols used on the internet.
    - The world wide web is a system of linked pages, programs, and files.
    - HTTP is a protocol used by the world wide web
    - The world wide web uses the internet

- Go over AP videos, vocabulary, and essential knowledge.  Draw a diagram showing the internet and its many levels. A preferred diagram would using your knowledge of frontend, backend, deployment, etc.  Picture would highlight vocabulary by illustration. The below illustration have some ideas

![Internet Map](https://user-images.githubusercontent.com/111486111/232373729-c244e504-b29b-4b21-b47a-23b50b1d9ff4.png)

![Internet pt 2](https://user-images.githubusercontent.com/111486111/232391011-0d1b204d-17b9-4a66-9ed2-ac66fc234020.png)

![Full Stack]({{site.baseurl}}/images/fullstack.png)


- Often we draw pictures of machines communicating over the Internet with arrows.  However, the real communication goes through protocol layers and the machine and then is trasported of the network.   For College Board and future Computer Knowledge you should become familiar with the following ...

```
     User Machine  <---> Frontend Server <---> Backend Server
    +-----------+         +-----------+         +-----------+
    |  Browser  |         |  GH Page  |         |   Flask   |
    +-----------+    ^    +-----------+    ^    +-----------+
    |    HTTP   |    |    |    HTTP   |    |    |    HTTP   |
    +-----------+    |    +-----------+    |    +-----------+
    |    TCP    |    |    |    TCP    |    |    |    TCP    |   
    +-----------+    |    +-----------+    |    +-----------+
    |     IP    |    V    |     IP    |    V    |     IP    |
    +-----------+         +-----------+         +-----------+
    |  Network  |  <--->  |  Network  |  <--->  |  Network  |
    +-----------+         +-----------+         +-----------+
```

The "http" layer is an application layer protocol in the TCP/IP stack, used for ***communication between web browsers and web servers***. It is the protocol used for transmitting data over the World Wide Web.

The "transport" layer (TCP) is responsible for providing reliable data transfer between applications running on different hosts.  The TCP protocol segments the data into smaller ***chunks called "segments"***. Each segment contains a sequence number that identifies its position in the original stream of data, as well as other control information such as source and destination port numbers, and checksums for error detection.

The "ip" layer is responsible for packetizing data received from the TCP layer of the protocol stack, and then ***encapsulating the data into IP packets***. The IP packets are then sent to the lower layers of the protocol stack for transmission over the network.

The "network" layer is responsible for ***routing data packets between networks*** using the Internet Protocol (IP). This layer handles tasks such as packet addressing and routing, fragmentation and reassembly, and ***network congestion*** control.


### Fault Tolerance
> Watch both Daily videos for 4.2

- Complete the network activity, summarize your understanding of fault tolerance.

Activity:
<img width="727" alt="image" src="https://user-images.githubusercontent.com/111486111/232398086-2f271180-d7e6-4935-8f59-472fcae91d8b.png">
<img width="721" alt="image" src="https://user-images.githubusercontent.com/111486111/232398365-d58c4748-024b-49a8-8931-7ab203d2503e.png">


Fault Tolerance is the safety of having multiple connections within a network between devices to ensure a route is available if a connection goes down. The more devices and connections there are in a network, the more secure the network is. In order for a network to be fault tolerant, ALL of the devices need at least two different connections to the network. That way, if one connection goes down, the given device still has a way to communicate with the other devices in the network.


### Parallel and Distributed Computing
> Review previous lecture on Parallel Computing and watch Daily vidoe 4.3.  Think of ways to make something in you team project to utilize Cores more effectively.  Here are some thoughts to add to your story of Computers and Networks...

- What is naturally Distributed in Frontend/Backend archeticture?  

    In frontend and backend architecture, data is naturally distributed to make both pages more efficient. Frontend and backend both have their own processes that they need to run to make the page/server run efficiently. Therefore, frontend and backend both use parallel processing to complete tasks/run processes quickly.

- Analyze this command in Docker: ```ENV GUNICORN_CMD_ARGS="--workers=1 --bind=0.0.0.0:8086"```.   Determine if there is options are options in this command for parallel computing within the server that runs python/gunicorn.  Here is an [article](https://medium.com/building-the-system/gunicorn-3-means-of-concurrency-efbb547674b7)

Within the server that runs python/gunicorn, the Python application is run once for each worker. In order to run parallel computing, you can input the command "gunicorn --workers=5 --threads=2 --worker-class=gthread main:app" into the terminal. Doing so allows each worker to have two treads, allowing for 10 concurrent requests instead of the previous 5. 


> Last week we discussed parallel computing on local machine.  There are many options.  Here is something to get parallel computing work with a tool called Ray.
- Review this [article](https://www.anyscale.com/blog/writing-your-first-distributed-python-application-with-ray)...  Can you get parallel code on images to work more effectively?  I have not tried Ray.

- Code example from ChatGPT using squares.  This might be more interesting if nums we generated to be a lot bigger.

```python
import ray

# define a simple function that takes a number and returns its square
def square(x):
    return x * x

# initialize Ray
ray.init()

# create a remote function that squares a list of numbers in parallel
@ray.remote
def square_list(nums):
    return [square(num) for num in nums]

# define a list of numbers to square
nums = [1, 2, 3, 4, 5]

# split the list into two parts
split_idx = len(nums) // 2
part1, part2 = nums[:split_idx], nums[split_idx:]

# call the remote function in parallel on the two parts
part1_result = square_list.remote(part1)
part2_result = square_list.remote(part2)

# get the results and combine them
result = ray.get(part1_result) + ray.get(part2_result)

# print the result
print(result)

```
