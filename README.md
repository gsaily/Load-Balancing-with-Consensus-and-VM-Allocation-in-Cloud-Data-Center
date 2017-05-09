# Load-Balancing-with-Consensus-and-VM-Allocation-in-Cloud-Data-Center
The project focuses on implementing load balancing within a cloud-based Data Center by
using consensus to allocate virtual machines within the data center.

#Technologies and Concepts used
CloudSim :I have used CloudSim, an open source Java-based simulator that has dedicated interfaces for VM, memory, bandwidth etc. It is easily configurable and allows for flexible unconstrained policy formulation and implementation for VM allocation and scheduling. 

Load Balancing : In cloud-based data centers, efficient resource provisioning and utilization are major concerns. In order to ensure service availability and reliability to the cloud users, efficiently allocating VMs to every host within the data center, to service both equal and unequal requests and applications, is very crucial. This should be done in a manner that ensures balance in the work being done on each host so that no host is overwhelmed with requests while other hosts may service comparatively lesser number of requests or are idle. Load balancing is essential for preventing congestion and for the provision of reliability and efficient resource utilization.

#Consensus Algorithms for Load Balancing:
1. First Fit Voting 
We begin with virtual machines that need to be allocated to hosts within a data center. Each host votes for the first virtual machine, in the list of currently available virtual machines, that it can hold. At the end of voting, a virtual machine can either have one vote or multiple votes. If it has one vote, that virtual machine is allocated to the only host that voted for it. If a Virtual Machine has multiple votes, we check for the utilization of the hosts that voted for it. The Virtual Machine is then allocated to the host which has the least utilization, which means the host has the maximum room for hosting the particular virtual machine. The remaining virtual machines which do not get voted on will be evenly allocated to the hosts in a round robin fashion based on host utilization.

2. Best Fit Voting
The initial idea begins with virtual machines that need to be allocated to hosts within a data center. Each host votes for the virtual machine with the largest size that it can afford to hold. The host picking the largest VM is part of the definition of best fit. At the end of voting, a virtual machine can either have one vote or multiple votes. If it has one vote, that Virtual Machine is allocated to the only host that voted for it. If a virtual machine has multiple votes, we check for the utilization of the hosts that voted for it. The Virtual Machine is then allocated to the host which has the least utilization, or the maximum room for hosting the particular virtual machine. The remaining virtual machines are evenly allocated to the hosts based on the hosts’ utilization.



