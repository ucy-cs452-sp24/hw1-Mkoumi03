Homework1 report
All measurements were made in a cluster of machines with two nodes in the Wisconsin datacenter using CloudLab.

1.	Local memory  (DRAM)
Latency and bandwidth to local memory DRAM were measured using the mlc tool. As seen from the mlc_ouput file, the latency to local memory for our machine is 96.1 ns and the bandwidth is 48581.2 mb/s. We can see that the total physical memory for the machine is 196670452 kb = ~ 196 Gb from the MemTotal tab in the meminfo_output file.

2.	Local disk
Latency and bandwidth to the local disk were measured using the ioping and fio commands respectively. From the disk_latency_output file we can see that the average latency for 20 disk requests was 232.7 us. From the disk_bandwidth_output file we can see that the bandwidth to the local disk is about 277 mbits/s = 34.6 mB/s. 
The capacity of the disk was measured using the hdparm tool as we can see from the disk_capacity_output file, the total capacity of the disk is 480 Gb. 

3.	Network
Network latency and bandwidth between two machines in the cluster was measured using the ping and iperf commands respectively. From the network_latency_output file we can see that the average latency for 20 requests from node0 to node1 is 0.058 ms per request. For the network bandwidth the command iperf was used at the clients interface using incremental bandwidth limit each time. From the network_bandwidth_output file we can see that the maximum limit for the bandwidth is 3.5 Gbits/s = 437.5 mb/s. 


Comments: 
From the above experiments we can see that the latency for the local memory DRAM is much lower than the latency to the disk. Also the bandwidth of the local memory is much higher then the bandwidth of the disk. That shows that the local memory is much more efficient regarding speed and the amount of data that can be transferred from and towards it, but the disk is much larger in size and can store much more data. 



