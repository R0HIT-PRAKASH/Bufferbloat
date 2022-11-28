1. Why do you see a difference in webpage fetch times with small and large router buffers?
   Ans. The reason the larger router buffer takes more time is because there is more space for a packet to
   have to wait in. A longer buffer means more packets have to wait in line, so each packet waits a longer
   time. On the other hand, the shorter buffer lets packets go through much quicker so the fetch time is shorter.

2. Bufferbloat can occur in other places such as your network interface card (NIC). Check the output of ifconfig eth0 on your VirtualBox VM. What is the (maximum) transmit queue length on the network interface reported by ifconfig? For this queue size and a draining rate of 100 Mbps, what is the maximum time a packet might wait in the queue before it leaves the NIC?
   Ans. The txqueuelen reported is 1000. The MTU is 1500bytes, so the maximum number of bytes in the queue at
   any given time is 1000\*1500 = 1500000 B = 12000000 b.
   At 100 Mbps, 12000000 b/100 Mbps = 12000000 b/100000000 bps = 0.12s

3. How does the RTT reported by ping vary with the queue size? Write a symbolic equation to describe the relation between the two (ignore computation overheads in ping that might affect the final result).
   Ans. There seems to be a positive correlation between the RTT and the queue size.

4. Identify and describe two ways to mitigate the bufferbloat problem.
   Ans.
