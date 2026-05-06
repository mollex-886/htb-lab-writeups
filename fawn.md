# Fawn - Hack The Box

## Difficulty
Very Easy

## Objective
Enumerate SMB shares and retrieve the flag.

---

## Step 1 - Scan the Target
Performed an Nmap scan to identify running services.

Command:
```bash
nmap -sV <target-ip>
```

### Result
The scan identified:
- Port 445 open
- SMB service enabled

---

## Step 2 - Enumerate SMB Shares
Used smbclient to check available SMB shares.

Command:
```bash
smbclient -L ////<target-ip>/
```

---

## Step 3 - Access the SMB Share
Connected to the accessible share using anonymous authentication.

Command:
```bash
smbclient ////<target-ip>/<share-name>
```

---

## Step 4 - Explore Files
Listed files inside the share and searched for the flag.

Commands:
```bash
ls
cd
get flag.txt
```

---

## Step 5 - Read the Flag
Opened the downloaded file locally.

Command:
```bash
cat flag.txt
```

---

## Skills Practiced
- SMB enumeration
- Anonymous authentication
- File share interaction
- Basic file retrieval

## Tools Used
- Nmap
- smbclient
