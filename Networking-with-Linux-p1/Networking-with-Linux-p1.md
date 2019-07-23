# Introduction to Networking with LINUX PART-1
## 1 INTRODUCTION
When it comes to networking, there is probably nothing that cannot
be done with Linux.

Some one said once : Programming is learnt better with examples
rather than with theories and books. Here are commands explained
with example. But don’t rely only on this article. This is only
the insight into what can be done. See manual pages for more
information.
## 2 ping
**send ICMP ECHO REQUEST to network hosts**

ping is the most basic command. And it is by default installed in all linux sys-
tems. This can be used to check if your internet connection is working properly.

![Figure 2.1](image/ping-google.png)

**Figure 2.1**

It verifies the connection by sending packets of data. Use ctrl-C to stop it
otherwise it will keep sending data. In the end it provides a brief summary of
what has been done. It sends 1 packet each second by default. here you can see
172.217.166.238 is the exact IP address of server. It also provides the length of
time taken to return data.

![Figure 2.2](image/ping-count.png)

**Figure 2.2**

Flag *-c* **n** specifies exactly n number of packets to send.
Afterwards the command auto stops.

![Figure 2.3](image/ping-intr-num.png)

**Figure 2.3**

Flag *-i* **n** specifies exactly n seconds wait before sending next packet.
And Flag *-n* says to print only numeric outputs.
As manual says: only superuser can set interval less than 0.2 .

There even more options, like you can set a deadline time for ping to stop
with *-w* **deadline**.
Default packet size is 55 but you can change it with *-s* **packetsize**.
#### NOTE :-
> Some network devices are configured to ignore these packets for security reasons.
  Even some firewalls are configured to block ICMP traffic.

> example site : w3schools.com .

> "ping w3schools.com" will fail to recieve any packets .

## ifconfig
**configure a network interface**

Ifconfig  is used to configure the kernel-resident network interfaces.
It is used at boot time to set up interfaces as necessary.
After that, it is usually only needed when debugging or 
when system  tuning  is needed.

![Figure 3.1](image/ifconfig.png)

**Figure 3.1**

If no arguments are given,
ifconfig displays the status of the currently active interfaces. 
If a single interface argument is given,
it displays the status of the given interface only.

![Figure 3.2](image/ifconfig-data.png)

**Figure 3.2**
    
Using grep to see a specific result.
Here I show data uses by the Ethernet Interface.
RX is recieved amount of data and TX is transfered data since last login.

## traceroute
**print the route packets trace to network host**

Trace every server that request jumps from or to in order to get to the host server.

![Figure 4.1](image/traceroute-thisp.png)

**Figure 4.1**
    
We see asterisks in the line when router do not provide identifying information.
In cases where routing information is blocked, we can sometimes overcome this by adding
either the -T or -I option to the traceroute command.
