


# 🚀 Process Visualization Tool

## 📖 Project Description
Tool for visualizing process scheduling.
The **Process Visualization Tool** is an interactive application designed to monitor system resources and simulate CPU scheduling algorithms in real-time. This project provides a user-friendly interface to help students, educators, and professionals understand complex operating system concepts, including process lifecycle management and CPU scheduling.

---

## 🌟 Key Features

### ⚡ CPU Scheduling Algorithms:
- **First-Come-First-Serve (FCFS)**
- **Shortest Job First (SJF)**
- **Round Robin (RR)**
- **Priority Scheduling**

### 📊 Real-Time Monitoring:
- Visualizes **CPU and memory usage**.
- Displays **active and pending processes**.

### 💻 User Interface:
- Interactive and intuitive **dashboard**.
- Light and dark themes for improved usability.

### 🖥️ Cross-Platform Support:
- Compatible with **Windows** and **macOS** systems.

### 🔔 Custom Alerts:
- Notifications for **resource overuse thresholds**.

---
## 📚 Algorithm Details

### ⏳ FCFS (First-Come-First-Serve):
- **Type**: Non-preemptive scheduling  
- **Mechanism**: Strict FIFO queue processing  
- **Key Traits**:
  - Simple implementation
  - Demonstrates convoy effect
  - No starvation
- **Visualization**: Sequential process blocks

### 🔍 SJF (Shortest Job First):
- **Variants**:
  - Non-preemptive (SJF)
  - Preemptive (SRTF - Shortest Remaining Time First)
- **Mechanism**: Priority queue sorted by burst time  
- **Key Traits**:
  - Optimal for minimum wait time
  - Shows starvation potential
  - Requires burst time prediction
- **Visualization**: Preemption alerts, burst time tooltips

### 🔄 Round Robin:
- **Core**: Time-slicing with quantum  
- **Mechanism**: Circular queue with preemption  
- **Key Traits**:
  - Configurable time quantum
  - Fair CPU allocation
  - High context switches
- **Visualization**: 
  - Quantum boundaries marked
  - Context switch counter

### ⚖️ Priority Scheduling:
- **Variants**:
  - Static vs dynamic priorities
  - Preemptive/non-preemptive
- **Mechanism**: Priority queue execution  
- **Key Traits**:
  - Critical for real-time systems
  - Shows priority inversion
  - Requires aging mechanism
- **Visualization**:
  - Priority color-coding
  - Starvation warnings
---
## 📊 CPU Scheduling Algorithms Comparison

| Algorithm          | Type       | Decision Mode | Preemptive? | Starvation? | Avg. Wait Time | Key Use Case                     |
|--------------------|------------|---------------|-------------|-------------|----------------|----------------------------------|
| **FCFS**           | Non-preemptive | Arrival Time   | ❌ No       | ❌ No       | High           | Batch systems                    |
| **SJF**            | Both       | Burst Time     | ✅ (SRTF)   | ✅ Possible | Lowest         | Interactive systems              |
| **Round Robin**    | Preemptive | Time Quantum   | ✅ Yes      | ❌ No       | Medium         | Time-sharing systems             |
| **Priority**       | Both       | Priority       | Optional    | ✅ Possible | Varies         | Real-time systems                |

### Key Characteristics:
1. **FCFS** (First-Come-First-Serve):
   - Simple but suffers from convoy effect
   - Example: `P1(24ms) → P2(3ms) → P3(3ms)` has avg wait time=17ms

2. **SJF** (Shortest Job First):
   - Optimal for minimum wait time but needs future knowledge
   - Preemptive version = SRTF (Shortest Remaining Time First)

3. **Round Robin**:
   - Each process gets CPU for fixed time quantum (e.g., 4ms)
   - Performance depends heavily on quantum size

4. **Priority**:
   - Can be preemptive or non-preemptive
   - Requires aging to prevent starvation

### 📝 When to Use:
- **FCFS**: When simplicity > performance
- **SJF/SRTF**: When burst times are predictable
- **Round Robin**: Fairness required (OS time-sharing)
- **Priority**: Urgent tasks need precedence
---

## 🛠️ Technologies Used

### **Programming Language:**
- Python

### **Libraries and Frameworks:**
- `PyQt5`
- `Psutil`
- `NumPy`
- `PyQtGraph`
- `Matplotlib`

### **Development Tools:**
- Qt Designer
- Visual Studio Code (VSCode)
- GitHub for version control

---

## 📦 How to Run the Project

### 1️⃣ Clone the Repository:
```bash
git clone https://github.com/your-username/process-visualization-tool.git
```

### 2️⃣ Open in VSCode:
- Open the project folder in **Visual Studio Code**.

### 3️⃣ Install Dependencies:
Ensure Python and all required libraries are installed on your system. Run:
```bash
pip install -r requirements.txt
```

### 4️⃣ Run the Application:
Execute the main script:
```bash
python main.py
```

---

## 📝 How to Use

1. Launch the application by running **main.py**.
2. Use the **interactive dashboard** to:
   - View real-time **CPU and memory usage graphs**.
   - Simulate CPU scheduling algorithms by selecting an option.
   - Customize process priorities and observe results.
3. Explore additional features like:
   - Light/dark themes.
   - Alerts for **resource overuse**.

---
## 🎥Video Demonstration

<video controls src="Screen Recording 2025-03-29 181344-1.mp4" title="Title"></video>

---

## 📷 Screenshots
### System Architecture:
![alt text](<diag.png>)

### 🔍 Real-Time Monitoring Dashboard:
![alt text](<Screenshot (56).png>)

### 📈 Scheduling Algorithm Visualization:
![alt text](<Screenshot (65).png>)

---

## 🚀 Future Enhancements

- Add more scheduling algorithms (e.g., **Multi-Level Queue Scheduling**, **Multi-Level Feedback Queue**).
- Implement **GPU monitoring capabilities**.
- Provide a **web-based version** for remote monitoring.
- Introduce **logging features** for historical data analysis.
- Optimize resource usage for handling large datasets.

---

## 🤝 Contributing

We welcome contributions! To contribute:

1. Fork the repository.
2. Create a new branch:
   ```bash
   git checkout -b feature/your-feature-name
   ```
3. Commit your changes:
   ```bash
   git commit -m "Add your feature description here"
   ```
4. Push to the branch:
   ```bash
   git push origin feature/your-feature-name
   ```
5. Open a pull request.

---

## 📄 License
This project is licensed under the **MIT License**. See the LICENSE file for details.

---

