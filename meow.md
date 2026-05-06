# Hack The Box Beginner Lab Writeups

## Meow.md

```md
# Meow - Hack The Box

## Difficulty
Very Easy

## Objective
Gain access to the target machine and retrieve the flag.

---

## Step 1 - Initial Scan
Started with an Nmap scan to identify open ports and running services.

Command used:
```bash
nmap -sV <target-ip>
```

### Result
- Port 23 open
- Service detected: Telnet

---

## Step 2 - Connect to Telnet Service
Connected to the Telnet service.

Command used:
```bash
telnet <target-ip>
```

---

## Step 3 - Login
Tried common/default credentials.

Successfully logged into the system.

---

## Step 4 - Locate the Flag
Navigated through the system directories to locate the flag file.

Commands used:
```bash
ls
pwd
cd
cat flag.txt
```

---

## Skills Practiced
- Nmap scanning
- Service enumeration
- Telnet access
- Basic Linux navigation

## Tools Used
- Nmap
- Telnet
- Linux CLI
```

---

# Fawn.md

```md
# Fawn - Hack The Box

## Difficulty
Very Easy

## Objective
Access the SMB share and retrieve the flag.

---

## Step 1 - Initial Scan
Performed an Nmap scan to identify open services.

Command used:
```bash
nmap -sV <target-ip>
```

### Result
- Port 445 open
- SMB service detected

---

## Step 2 - SMB Enumeration
Enumerated available SMB shares.

Command used:
```bash
smbclient -L //<target-ip>/
```

---

## Step 3 - Anonymous Login
Connected using anonymous access.

Command used:
```bash
smbclient //<target-ip>/<share-name>
```

---

## Step 4 - Retrieve the Flag
Listed files and opened the flag.

Commands used:
```bash
ls
get flag.txt
cat flag.txt
```

---

## Skills Practiced
- SMB enumeration
- Anonymous authentication
- File share interaction

## Tools Used
- Nmap
- smbclient
```

---

# Dancing.md

```md
# Dancing - Hack The Box

## Difficulty
Very Easy

## Objective
Enumerate SMB shares and retrieve the flag.

---

## Step 1 - Scan the Target
Used Nmap to identify open ports and services.

Command used:
```bash
nmap -sV <target-ip>
```

### Result
- SMB ports detected
- Windows machine identified

---

## Step 2 - Enumerate SMB Shares
Checked available SMB shares.

Command used:
```bash
smbclient -L //<target-ip>/
```

---

## Step 3 - Access the Share
Connected to the accessible share.

Command used:
```bash
smbclient //<target-ip>/<share-name>
```

---

## Step 4 - Navigate Through Directories
Explored folders to locate the flag.

Commands used:
```bash
ls
cd
get
```

---

## Step 5 - Read the Flag
Opened the downloaded file locally.

Command used:
```bash
cat flag.txt
```

---

## Skills Practiced
- SMB enumeration
- Windows share interaction
- File navigation

## Tools Used
- Nmap
- smbclient
```

---

# Redeemer.md

```md
# Redeemer - Hack The Box

## Difficulty
Very Easy

## Objective
Interact with the Redis service and retrieve the flag.

---

## Step 1 - Initial Scan
Performed an Nmap scan.

Command used:
```bash
nmap -sV <target-ip>
```

### Result
- Port 6379 open
- Redis service detected

---

## Step 2 - Connect to Redis
Connected to the Redis server.

Command used:
```bash
redis-cli -h <target-ip>
```

---

## Step 3 - Enumerate Redis Data
Viewed available keys.

Commands used:
```bash
INFO
KEYS *
```

---

## Step 4 - Retrieve the Flag
Accessed the stored value containing the flag.

Command used:
```bash
GET <key-name>
```

---

## Skills Practiced
- Redis interaction
- Service enumeration
- Basic database querying

## Tools Used
- Nmap
- redis-cli
```

