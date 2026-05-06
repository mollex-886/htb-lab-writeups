# Meow - Hack The Box

## Difficulty
Very Easy

## Objective
Enumerate the target machine, gain access through the exposed service, and retrieve the flag.

---

## Step 1 - Scan the Target
Started with an Nmap scan to identify open ports and services.

Command:
```bash
nmap -sV <target-ip>
```

### Result
The scan showed:
- Port 23 open
- Service: Telnet

---

## Step 2 - Connect to the Service
Since Telnet was open, connected to the machine using Telnet.

Command:
```bash
telnet <target-ip>
```

---

## Step 3 - Login to the System
Tested common/default login options.

Successfully gained access to the system.

---

## Step 4 - Explore the Machine
Used basic Linux commands to navigate through directories and search for the flag file.

Commands:
```bash
ls
pwd
cd
find / -name flag.txt 2>/dev/null
```

---

## Step 5 - Read the Flag
Displayed the contents of the flag file.

Command:
```bash
cat flag.txt
```

---

## Skills Practiced
- Service enumeration
- Telnet access
- Basic Linux navigation
- File searching

## Tools Used
- Nmap
- Telnet
- Linux CLI
