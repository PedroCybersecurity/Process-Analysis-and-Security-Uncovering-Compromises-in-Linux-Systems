# Process-Analysis-and-Security-Uncovering-Compromises-in-Linux-Systems
This project documents a vital cybersecurity practice of monitoring and analyzing process information on Linux systems to detect potential compromises. Utilizing the ps command, we delve into identifying suspicious processes that could indicate a system breach.

This guide provides a step-by-step methodology for security analysts to efficiently scrutinize process statuses, memory usage, and parent processes to safeguard their network.

### README.md Content:

```markdown
# Process Analysis and Security: Uncovering Compromises in Linux Systems

## Introduction
In the landscape of cybersecurity, vigilance in monitoring system processes is crucial for early detection of unauthorized activities and potential system compromises. This guide focuses on leveraging the `ps` command in Linux to analyze process information, offering insights into identifying and responding to suspicious processes.

## Objective
The primary aim is to equip security analysts with the knowledge to use the `ps` command for detailed process analysis. This involves examining process IDs (PIDs), states, memory usage, and parent processes to identify anomalies that may suggest a system compromise.

## Tools and Technologies
- **Linux Terminal**: The command-line interface used for executing system commands.
- **ps command**: A utility for displaying current process information on a Unix/Linux system.

## Process Overview

### Viewing and Analyzing Processes

1. **Accessing the Terminal**:
   - Open the Terminal application from the Favorites bar or your Linux distribution's application menu.

2. **Executing the ps Command**:
   - To view a comprehensive list of processes, execute:
     ```
     ps aux | less
     ```
   - This command displays all running processes with detailed information, including the user running the process, PID, CPU and memory usage, process start time, and the command that initiated the process.

### Key Components of the ps Command

- **a**: Show processes for all users.
- **u**: Display the process's user/owner.
- **x**: Include processes not attached to a terminal.
- **| less (or | more)**: Paginate the output for easier viewing.

### Analyzing Suspicious Processes

- **Identify the PID**: The Process ID is a unique identifier for a running process. For example, to find the PID for the `hald` process, look for its entry in the `ps` output.
- **Process State**: Look for the state of specific processes, such as `./shell.elf`. A running state can be normal, but in the context of unknown or suspicious processes, further investigation is warranted.
- **Memory Usage**: High memory usage by unfamiliar processes can be a red flag. The `ps` output includes the percentage of memory used by each process.
- **Parent Process**: Determining which command invoked a process (e.g., PID 1857 being invoked by `python`) can help trace back to potentially malicious activities.

## Questions and Analysis

- Through careful observation of process details provided by `ps`, answer targeted questions about process IDs, states, memory usage, and parent commands to gauge the security posture of the system.

## Conclusion

Regular monitoring and analysis of system processes are pivotal in maintaining a secure Linux environment. By mastering the `ps` command and understanding its output, security analysts can effectively spot and investigate suspicious activities, thereby strengthening their organization's defense against compromises.

## Recommendations

- Continuously monitor system processes and resource usage.
- Implement automated tools for real-time anomaly detection.
- Conduct regular system audits and security training for IT staff.

Stay secure and vigilant!
```
