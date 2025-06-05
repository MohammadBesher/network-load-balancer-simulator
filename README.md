Network Load Balancer Simulator with AI Algorithms
Project Overview
The Network Load Balancer Simulator with AI Algorithms is a comprehensive simulation tool designed to model and optimize network traffic routing using various load balancing algorithms. The system simulates a real-time distributed network, allowing you to evaluate how different load balancing strategies—such as Round Robin, Least Connections, and Reinforcement Learning (RL)—handle traffic under various conditions.

This project is ideal for those interested in networking, AI, and systems programming. It provides insights into network performance optimization, AI-based routing, and traffic management, with practical applications in distributed systems and cloud computing.

Features
Real-Time Network Simulation:

Simulates a distributed network with multiple servers and clients, where messages are routed based on dynamically chosen load balancing algorithms.

TCP/UDP Communication:

Supports both TCP (reliable, connection-oriented) and UDP (unreliable, connectionless) protocols, enabling the simulation of both reliable and fast, low-latency communication scenarios.

Dynamic Load Balancing Algorithms:

Round Robin: Distributes traffic evenly across servers in a cyclic manner, ensuring fair load distribution.

Least Connections: Routes messages to the server with the fewest active connections, optimizing server load.

Reinforcement Learning (RL): Uses Q-learning to adapt the system's behavior over time based on traffic patterns and performance feedback.

Randomized Network Topology:

Generates random network topologies with user-defined parameters (e.g., number of servers and connections), providing a flexible simulation environment for various real-world network scenarios.

Simulate Real-World Traffic:

Simulates real-time traffic patterns, including TCP three-way handshakes and UDP packet loss, allowing you to assess how each algorithm performs under realistic conditions.

Performance Metrics and Reporting:

Tracks key metrics such as response time, throughput, packet loss, and server load for each simulation.

Generate detailed CSV reports for performance analysis and comparison between algorithms.

Thread Safety:

Implements mutexes and threading for concurrent message processing and real-time simulation, ensuring thread safety in multi-threaded environments.

Why Is This Project Useful?
This project offers a practical understanding of network traffic management and optimization. It's particularly useful for:

Learning about load balancing: See how different algorithms distribute traffic and balance server load in real-world distributed systems.

Simulating TCP/UDP traffic: Understand how protocols like TCP and UDP differ in terms of reliability, latency, and performance.

Applying Reinforcement Learning (RL) to dynamic traffic routing: See how AI algorithms can adapt to changing network conditions and improve routing decisions over time.

Evaluating system performance: Measure the efficiency of various load balancing algorithms in handling network traffic, and identify the most optimal strategies for different scenarios.

Technologies and Tools Used
Languages: C++, C++ Standard Library (STL), Multithreading, Mutexes

Algorithms: Load Balancing, Reinforcement Learning (Q-learning), Traffic Simulation

Libraries/Frameworks: C++ STL containers (vectors), I/O for data processing, and threading libraries for concurrency

Tools: Compiler (g++), Git for version control, Visual Studio Code (IDE)

Installation Instructions
Clone the repository:

bash
Copy
git clone https://github.com/yourusername/network-load-balancer-simulator.git
Navigate to the project directory:

bash
Copy
cd network-load-balancer-simulator
Compile the project:

bash
Copy
g++ -o load_balancer main.cpp clean_ddos_data.cpp LoadBalancer.cpp RoundRobinLoadBalancer.cpp RLLoadBalancer.cpp LeastConnectionsLoadBalancer.cpp PerformanceMetrics.cpp TrafficLogProcessor.cpp
Run the simulation:

bash
Copy
./load_balancer
Usage Instructions
Create Network Topology:

Specify the number of servers and connections for a randomized network topology.

Choose Load Balancer Algorithm:

Select from Round Robin, Least Connections, or Reinforcement Learning (RL) for routing decisions.

Select Protocol:

Choose TCP (for reliable communication with handshake) or UDP (for fast, unreliable communication).

Simulate Traffic:

The program will route messages between servers using the selected algorithm and protocol, displaying real-time performance metrics.

View Metrics:

Real-time metrics like response time, throughput, and server load are displayed for each algorithm.

Generate Reports:

After the simulation, the program will generate a CSV report containing performance data for analysis.

Performance Metrics
Response Time: Time taken for the request to travel from the client to the server.

Throughput: Amount of data handled by the server in a given time period.

Packet Loss: Percentage of packets lost during UDP communication.

Server Load: The amount of active connections or processing capacity utilized by each server.

Sample Usage
1. Running the Simulation
After compiling the project, run the simulation from the terminal. The program will prompt you to:

Create a network topology.

Choose a load balancer algorithm (Round Robin, Least Connections, RL).

Select TCP or UDP as the communication protocol.

Simulate the traffic and view the metrics.

2. Example Output:
plaintext
Copy
----------------------------------
Network Load Balancer Simulator
1. Create Random Network Topology
2. Choose Load Balancer Algorithm
3. Choose Protocol (TCP/UDP)
4. Simulate Traffic
5. Display Metrics
6. Generate Report
7. Exit
----------------------------------
Enter choice: 1
Enter number of servers (nodes): 5
Enter number of connections (edges): 6
Node 0: 1 4 
Node 1: 0 2 3
Node 2: 1 4
Node 3: 1 4
Node 4: 0 2 3
----------------------------------
Enter choice: 2
Choose Load Balancer Algorithm:
1. Round Robin
2. Least Connections
3. Reinforcement Learning
Enter choice: 3
----------------------------------
Enter choice: 3
Choose Protocol:
1. TCP
2. UDP
Enter choice: 1
----------------------------------
Simulating TCP connection from 0 to 3
TCP handshake complete. Sending message of size 10 bytes.
Simulating UDP message from 1 to 4
UDP packet of size 5 bytes sent successfully.
----------------------------------
Round Robin Load Balancer Metrics
Average Response Time: 0.25
Throughput: 100 MB/s
----------------------------------
3. Generating a Report
After running the simulation, generate a performance report:

bash
Copy
$ ./load_balancer
Enter choice: 6
Report generated: network_performance_report.csv
The CSV report will look like this:

csv
Copy
Protocol,Load Balancer,Response Time,Throughput
TCP,Round Robin,0.25,100
UDP,Least Connections,0.15,120
TCP,RL,0.20,110
License
This project is licensed under the MIT License.

Conclusion
The Network Load Balancer Simulator is a powerful tool for understanding and experimenting with different load balancing algorithms and their impact on real-time network performance. By simulating both TCP and UDP traffic and using Reinforcement Learning for decision-making, this project provides valuable insights into optimizing network routing in distributed systems. It's a great project for anyone interested in networking, AI, and systems programming.

