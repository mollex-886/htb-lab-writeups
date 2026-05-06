# Redeemer - Hack The Box

## Difficulty
Very Easy

## Objective
Enumerate the Redis service and retrieve the stored flag.

---

## Step 1 - Scan the Target
Performed an Nmap scan to identify open services.

Command:
```bash
nmap -sV <target-ip>
```

### Result
The scan revealed:
- Port 6379 open
- Redis service detected

---

## Step 2 - Connect to Redis
Connected to the Redis database using redis-cli.

Command:
```bash
redis-cli -h <target-ip>
```

---

## Step 3 - Enumerate the Database
Gathered information about the Redis server.

Commands:
```bash
INFO
```

Checked available keys.

Command:
```bash
KEYS *
```

---

## Step 4 - Retrieve the Flag
Retrieved the value stored in the discovered key.

Command:
```bash
GET <key-name>
```

---

## Step 5 - Read the Flag
Displayed the flag output returned by Redis.

---

## Skills Practiced
- Service enumeration
- Redis interaction
- Basic database querying
- Information gathering

## Tools Used
- Nmap
- redis-cli
