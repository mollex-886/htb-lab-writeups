# Dancing - Hack The Box

## Difficulty
Very Easy

## Objective
Enumerate SMB shares on a Windows machine and retrieve the flag.

---

## Step 1 - Scan the Machine
Started with an Nmap scan to identify services.

Command:
```bash
nmap -sV <target-ip>
```

### Result
The scan showed:
- SMB-related ports open
- Windows operating system detected

---

## Step 2 - Enumerate SMB Shares
Checked available shares using smbclient.

Command:
```bash
smbclient -L //<target-ip>/
```

---

## Step 3 - Access the Share
Connected to the accessible SMB share.

Command:
```bash
smbclient //<target-ip>/<share-name>
```

---

## Step 4 - Navigate Through Directories
Explored directories to locate important files.

Commands:
```bash
ls
cd
pwd
```

---

## Step 5 - Download the Flag
Downloaded the flag file from the share.

Command:
```bash
get flag.txt
```

---

## Step 6 - Read the Flag
Viewed the contents of the downloaded flag file.

Command:
```bash
cat flag.txt
```

---

## Skills Practiced
- SMB enumeration
- Windows share interaction
- File navigation
- File retrieval

## Tools Used
- Nmap
- smbclient
