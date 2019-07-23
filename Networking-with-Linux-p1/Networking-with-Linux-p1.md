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

![Figure 2.1](/image/ping-google.png)
Format: ![Alt Text](url)

It verifies the connection by sending packets of data. Use ctrl-C to stop it
otherwise it will keep sending data. In the end it provides a brief summary of
what has been done. It sends 1 packet each second by default. here you can see
172.217.166.238 is the exact IP address of server. It also provides the length of
time taken to return data.

![Figure 2.2](/image/ping-count.png)
Format: ![Alt Text](url)

Flag *-c* **n** specifies exactly n number of packets to send.
Afterwards the command auto stops.

![Figure 2.3](/image/ping-intr-num.png)
Format: ![Alt Text](url)

Flag *-i* **n** specifies exactly n seconds wait before sending next packet.
And Flag *-n* says to print only numeric outputs.
As manual says: only superuser can set interval less than 0.2 .
There even more options, like you can set a deadline time for ping to stop
with *-w* **deadline**.
Default packet size is 55 but you can change it with *-s* **packetsize**.
#### NOTE :-
> Some network devices are configured to ignore these packets for security reasons. Even some firewalls are configured to block ICMP traffic.
> example site : w3schools.com .
> "ping w3schools.com" will fail to recieve any packets .
