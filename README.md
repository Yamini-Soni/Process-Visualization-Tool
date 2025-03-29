# 🚀 Process Visualization Tool

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Python 3.8+](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/)
![Platform](https://img.shields.io/badge/Platform-Windows%20|%20macOS%20|%20Linux-lightgrey)
[![Contributor Covenant](https://img.shields.io/badge/Contributor%20Covenant-2.1-4baaaa.svg)](CODE_OF_CONDUCT.md)

## 📖 Table of Contents
- [Project Description](#-project-description)
- [Key Features](#-key-features)
- [Algorithm Details](#-algorithm-details) 
- [Installation](#-installation)
- [Usage](#-usage)
- [Technologies](#-technologies-used)
- [Demonstration](#-demonstration)
- [Contributing](#-contributing)
- [Troubleshooting](#-troubleshooting)
- [License](#-license)


## 📖 Project Description
The **Process Visualization Tool** is an interactive application that:
- Monitors system resources in real-time
- Simulates CPU scheduling algorithms
- Provides educational visualization of OS concepts
- Supports Windows, macOS, and Linux platforms


## 🌟 Key Features
### ⚡ Core Functionality
| Feature | Technical Implementation |
|---------|--------------------------|
| **Real-Time Monitoring** | 1-second refresh via `psutil` |
| **4 Scheduling Algorithms** | FCFS, SJF, Round Robin, Priority |
| **Cross-Platform** | Native OS implementations |
| **Educational Visualizations** | Gantt charts with matplotlib |

### 📊 Supported Platforms
| OS | Version | Status |
|----|---------|--------|
| Windows | 10/11 | ✅ Verified |
| macOS | 12+ (Intel/Apple Silicon) | ✅ Verified |
| Linux | X11/Wayland | ✅ Experimental |

### 💻 User Interface:
- Interactive and intuitive **dashboard**.
- Light and dark themes for improved usability.
- Custom alert thresholds for resources
- Tooltips and educational annotations

### 🔔 Custom Alerts:
- Notifications for **resource overuse thresholds**.

### 📊 Supported Algorithms
1. **FCFS** (First-Come-First-Serve)
2. **SJF** (Shortest Job First)
3. **Round Robin** (Configurable quantum)
4. **Priority Scheduling**

## 📚 Algorithm Details

### Comparative Analysis

| Algorithm          | Type       | Decision Mode | Preemptive? | Starvation? | Avg. Wait Time | Key Use Case                     |
|--------------------|------------|---------------|-------------|-------------|----------------|----------------------------------|
| **FCFS**           | Non-preemptive | Arrival Time   | ❌ No       | ❌ No       | High           | Batch systems                    |
| **SJF**            | Both       | Burst Time     | ✅ (SRTF)   | ✅ Possible | Lowest         | Interactive systems              |
| **Round Robin**    | Preemptive | Time Quantum   | ✅ Yes      | ❌ No       | Medium         | Time-sharing systems             |
| **Priority**       | Both       | Priority       | Optional    | ✅ Possible | Varies         | Real-time systems                |


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
- Python Version 3.8+

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
## 🛠️ Installation

### All Platforms
```bash
# 1. Clone the repository
git clone https://github.com/your-repo/process-visualization-tool.git
cd process-visualization-tool

# 2. Create virtual environment
python -m venv venv

# 3. Activate environment
source venv/bin/activate  # Linux/macOS
.\venv\Scripts\activate   # Windows

# 4. Install dependencies
pip install --upgrade pip
Ensure Python and all required libraries are installed on your system. Run:
```bash
pip install -r requirements.txt
# 5. Run the Application:
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
<div align="center">
  <a href="https://youtu.be/SnHwQHs5gQI">
    <img src="https://img.youtube.com/vi/SnHwQHs5gQI/0.jpg" alt="Demo Video" width="50%">
  </a>
</div>

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
## 🖥️ Usage

### ⌨️ Keyboard Shortcuts
| Shortcut          | Action                | Platform Support       |
|-------------------|-----------------------|------------------------|
| <kbd>Ctrl</kbd> + <kbd>R</kbd> | Refresh Process List  | All Platforms          |
| <kbd>Ctrl</kbd> + <kbd>D</kbd> | Toggle Dark Mode      | Windows/Linux          |
| <kbd>Cmd</kbd> + <kbd>D</kbd>  | Toggle Dark Mode      | macOS                  |
| <kbd>F1</kbd>     | Show Help Panel       | All Platforms          |

### 🖱️ UI Controls
| Element           | Functionality                          |
|-------------------|----------------------------------------|
| **Algorithm Dropdown** | Select scheduling simulation mode      |
| **Priority Sliders**   | Adjust process priority levels (1-10)  |
| **Theme Toggle**  | Switch light/dark/cyberpunk themes     |

### 🎛️ CLI Options
```bash
# Basic usage
python main.py 

# Advanced options
python main.py \
  --theme dark \          # dark/light/cyberpunk
  --refresh 2000 \       # Update interval (ms)
  --quantum 4            # RR time quantum (ms)
```

---
## 🤝 Contributing [![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)

### 📌 Development Workflow

1. **Branch Naming Convention**  
   ```bash
   # Feature development
   git checkout -b feat/mlq-scheduler
   
   # Bug fixes
   git checkout -b fix/windows-dpi-scaling
   
   # Documentation
   git checkout -b docs/algorithm-examples

We welcome contributions!
To contribute:

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
## 🛠️ Troubleshooting

### Windows Issues
- **Missing DLLs**: Install [Visual C++ Redistributable](https://aka.ms/vs/17/release/vc_redist.x64.exe)
- **DPI Scaling**: Add manifest file for proper high-DPI display scaling
- **Admin Privileges**: Right-click → "Run as administrator" if getting access errors

### macOS Issues
- **Permission Errors**: Grant Terminal "Full Disk Access" in System Preferences → Security & Privacy
- **Apple Silicon**: Use `arch -x86_64 python3 main.py` for Rosetta 2 compatibility
- **Dark Mode**: Ensure `NSRequiresAquaSystemAppearance` is not set in Info.plist

### Linux Issues
- **Missing Packages**: Install `python3-tk` for GUI components
- **Wayland Support**: Run with `GDK_BACKEND=x11` if experiencing graphical glitches
- **Systemd Integration**: Use `--user` flag for non-root process monitoring

### Cross-Platform Issues
- **Virtual Environment**: Always activate with `source venv/bin/activate` (Linux/macOS) or `.\venv\Scripts\activate` (Windows)
- **Dependencies**: Use `pip install --prefer-binary` to avoid compilation issues
- **Firewall**: Add Python to allowed apps if connection-related errors occur
---
## 📄 License
This project is licensed under the **MIT License**. See the LICENSE file for details.

---
