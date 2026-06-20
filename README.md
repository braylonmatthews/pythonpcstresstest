# Bray Stress Test Suite

A Python hardware utility designed to monitor live system metrics, saturate multi-core processors, and optimize system resource allocation in real-time.


# Core Features

* **Hardware-Agnostic Telemetry:** Dynamically discovers the host machine's graphics hardware (NVIDIA, AMD, or Intel) at initialization via OS kernel sub-processes.
* **Asynchronous Data Pipeline:** Offloads hardware polling to a background daemon thread to keep the Tkinter graphical interface fluid and responsive.
* **True Multi-Core Stress Tester:** Spawns distinct operating system processes via the `multiprocessing` module to bypass Python's Global Interpreter Lock (GIL) and hit 100% core saturation.
* **Game Mode Optimizer:** Scans active system tasks and safely scales down the CPU scheduling priority of non-essential background applications (like web browsers and chat clients).


## Prerequisites & Installation

1. Ensure you have **Python 3.10+** installed on your operating system.
2. Open your terminal and install the required low-level hardware communication libraries:
   ```bash
   pip install psutil gputil
