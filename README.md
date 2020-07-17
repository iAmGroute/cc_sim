# Congestion Control Simulator

### [Live version :checkered_flag:](https://iamgroute.github.io/cc_sim/public/index.html)

### Instructions

##### This is a simulation of what happens when you want to send data over a network and are limited by the bandwidth of one intermediate link (the bottleneck).

For example, you want to send a big file (which ideally would be sent instantly) but your internet connection is limited to a maximum speed. You don't know what that speed is (and might change over time, as many flows use the same link) so you need to figure that out dynamically. This is the job of the congestion control algorithm. In this "game", that's your job!

- You control the sending rate (<b style="color: #822">red line</b>), with the vertical position of your mouse.
- The <b style="color: #282">green line</b> is the latency you measure when a reply (ACK) to a packet you sent arrives. It is the delay between the time you sent the packet, and the time the ACK arrived. Ideally, this will be equal to 1 round trip time (RTT).
- The <b style="color: #228">blue line</b> is the throughput you measure when a reply (ACK) to a packet you sent arrives. It is the rate at which the receiver receives the packets you sent, delayed by the time it takes for the ACK to arrive.
- The <b style="color: #E82">orange line</b> is the number of packets in the queue of the router/switch that has the bottleneck link. As you (temporarily) send packets faster than can be forwarded through that link, they need to stay in the queue and wait for the previous packets to be sent first.
- The <b style="color: #222">black line</b> is the bandwidth of the bottleneck link. It might randomly change form time to time!

You can use the buttons on the right to toggle some features on and off:

- The **'H'** button **hides** the queue size and bandwidth lines. You can't see these in the real world, so make sure to hide them once you figure out what's happening!
- The **'A'** button activates the **assist** feature, which adds some ripple to your output to help probing for bandwidth changes.

Your goal is to keep the <b style="color: #282">latency</b> as low as possible, while keeping the <b style="color: #228">throughput</b> as high as possible.

### Screenshots

![Screenshot 01](screenshots/scrot_01.png?raw=true)
![Screenshot 02](screenshots/scrot_02.png?raw=true)

