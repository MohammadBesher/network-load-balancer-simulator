
# AI-Based Network Load Balancer Simulator

## Project Overview
The **AI-Based Network Load Balancer Simulator** is a real-time network traffic simulator designed to model and optimize network traffic routing using **AI-based load balancing algorithms**. The system simulates a network of servers and clients, where messages are routed dynamically based on different load balancing strategies such as **Round Robin**, **Least Connections**, and **Reinforcement Learning (RL)**. The system supports **TCP** (reliable) and **UDP** (unreliable) communication protocols and can...

---

## Key Features:
- **AI-based Decision Making**: Implemented **Reinforcement Learning (Q-learning)** to optimize load balancing decisions over time, allowing the system to adapt based on traffic patterns and server performance.
- **Network Simulation**: Built a **randomized network topology** with multiple **nodes** (servers) and **edges** (connections) to simulate a distributed environment with dynamic traffic routing.
- **TCP and UDP Protocols**: Simulated both **reliable (TCP)** and **unreliable (UDP)** communication, comparing performance under different network conditions.
- **Dynamic Traffic Management**: Used **load balancing algorithms** (Round Robin, Least Connections, and RL) to distribute traffic efficiently based on real-time server load, message size, and protocol type.
- **Metrics and Reporting**: Tracked key performance metrics such as **response time**, **throughput**, **packet loss**, and **server load**. Generated **CSV reports** for performance comparison and analysis.

---

## Technologies:
- **Languages**: C++
- **Concepts**: Load Balancing, Reinforcement Learning, AI, Networking (TCP/UDP), Multi-threading, Mutexes
- **Tools**: Git, g++, Visual Studio Code

---

## Why It’s Important:
This project showcases the ability to apply **AI algorithms** to **networking** problems, simulating realistic **network traffic** and **routing decisions**. It provides practical insights into how AI can optimize network resource allocation in **distributed systems**, offering value for real-world applications like **cloud computing**, **edge networks**, and **Internet of Things (IoT)**.

---

## Installation Instructions:
1. **Clone the repository**:
   ```bash
   git clone https://github.com/yourusername/network-load-balancer-simulator.git
   ```

2. **Navigate to the project directory**:
   ```bash
   cd network-load-balancer-simulator
   ```

3. **Compile the project**:
   ```bash
   g++ -o load_balancer main.cpp clean_ddos_data.cpp LoadBalancer.cpp RoundRobinLoadBalancer.cpp RLLoadBalancer.cpp LeastConnectionsLoadBalancer.cpp PerformanceMetrics.cpp TrafficLogProcessor.cpp
   ```

4. **Run the simulation**:
   ```bash
   ./load_balancer
   ```

---

## Usage Instructions:
1. **Create Network Topology**:
   - Specify the **number of servers** and **connections** for a randomized network topology.

2. **Choose Load Balancer Algorithm**:
   - Select from **Round Robin**, **Least Connections**, or **Reinforcement Learning (RL)** for routing decisions.

3. **Select Protocol**:
   - Choose **TCP** (for reliable communication with handshake) or **UDP** (for fast, unreliable communication).

4. **Simulate Traffic**:
   - The program will route messages between servers using the selected algorithm and protocol, displaying real-time performance metrics.

5. **View Metrics**:
   - Real-time metrics like **response time**, **throughput**, and **server load** are displayed for each algorithm.

6. **Generate Reports**:
   - After the simulation, the program will generate a **CSV report** containing performance data for analysis.

---

## Performance Metrics:
- **Response Time**: Time taken for the request to travel from the client to the server.
- **Throughput**: Amount of data handled by the server in a given time period.
- **Packet Loss**: Percentage of packets lost during UDP communication.
- **Server Load**: The amount of active connections or processing capacity utilized by each server.

---

## Sample Usage:

### Running the Simulation:
After compiling the project, run the simulation from the terminal. The program will prompt you to:
- Create a network topology.
- Choose a load balancer algorithm (Round Robin, Least Connections, RL).
- Select TCP or UDP as the communication protocol.
- Simulate the traffic and view the metrics.

### Example Output:
```plaintext
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
```

### Generating a Report:
After running the simulation, generate a **performance report**:
```bash
$ ./load_balancer
Enter choice: 6
Report generated: network_performance_report.csv
```

The CSV report will look like this:
```csv
Protocol,Load Balancer,Response Time,Throughput
TCP,Round Robin,0.25,100
UDP,Least Connections,0.15,120
TCP,RL,0.20,110
```

---

## License:
This project is licensed under the **MIT License**.

