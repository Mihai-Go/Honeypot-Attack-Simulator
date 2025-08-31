# Honeypot Attack Simulator

A Python-based tool that generates realistic attack patterns to test security monitoring and honeypot response capabilities.  
Perfect for cybersecurity students and professionals to safely test their defenses in a lab environment.

## Features

- Simulates connections to common ports (FTP, SSH, HTTP, etc.)
- Generates fake brute-force login attempts
- Configurable intensity levels: `low`, `medium`, or `high`
- Continuous, threaded execution for realistic attack patterns
- Built using only the Python standard library

## Usage

1.  **Run the simulator from your terminal:**

    ```bash
    python3 Honeypot-Attack-Simulator.py --target <TARGET_IP> --intensity <low|medium|high> --duration <SECONDS>
    ```

2.  **Example command:**

    ```bash
    python3 Honeypot-Attack-Simulator.py --target 192.168.1.100 --intensity high --duration 600
    ```

### Command Line Arguments

- `--target`: IP address of the target honeypot (default: `127.0.0.1`)
- `--intensity`: Simulation intensity level (default: `medium`)
- `--duration`: Simulation length in seconds (default: `300`)

3.  **To stop the simulation early, press `CTRL + C` in the terminal.**

---

### How It Works

- The script uses threading to simulate multiple concurrent attacks.
- It targets a list of common ports to mimic real-world scanning behavior.
- Depending on the chosen intensity, it varies the speed and volume of connection attempts.
- All actions are printed to the console, providing a live view of the simulated attack.

## Learning Outcomes

- Understanding common network attack patterns
- Testing and validating honeypot configurations and log collection
- Working with Python's `argparse` for command-line interfaces
- Using threading to simulate concurrent events

## Next Steps

- Add more attack vectors (e.g., HTTP paths, user-agent strings)
- Export activity logs to a file for later analysis
- Simulate attacks from a list of random fake IP addresses for more realism

---

**Disclaimer**  
This tool is intended for educational and testing purposes only.  
Always ensure you have explicit permission before targeting any system.

**License**  
MIT License
