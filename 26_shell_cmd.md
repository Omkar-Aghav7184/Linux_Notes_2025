# 🐚 Shell Process ID and Nested Shells in Linux

## ✅ `echo $$` – Display Shell Process ID (PID)

The `$$` is a **special shell variable** that holds the **Process ID (PID)** of the current shell session.

### 🔧 Command:

```bash
echo $$

🔎 Purpose:
Identifies the current shell process

Useful for debugging, process management, or shell scripting

📌 Example Output:
Shell Type	PID
First shell's PID	316
Nested shell's PID	482
Second shell (terminal 2)	446

✅ bash – Starting a Nested Shell
Running the bash command inside an already running shell starts a new child shell (nested shell).

The nested shell has its own independent PID

Exiting this shell returns you to the parent shell

📌 Example Flow:
Step	Description	PID
Original shell start	Main shell window	316
bash command run	Nested shell inside the first one	482
exit from nested shell	Back to the original shell	316

✅ Multiple Shells / Terminals
Each WSL (Windows Subsystem for Linux) terminal window runs an independent shell process.

Running echo $$ in different terminals gives different PIDs

Confirms that these terminals are independent and parallel

📌 Example:
Terminal	PID
First WSL shell	316
Second WSL shell	446

🔁 Summary Table
Operation	Description	PID
First shell start	Main shell window	316
Nested bash	New shell inside the first one	482
After exit	Returned to original parent shell	316
Second shell	Separate shell window (terminal 2)	446

# 🔍 Process Monitoring with `ps -f` and `pstree -p` in Linux (WSL)

## ✅ `ps -f` – Full-format Listing of Processes

The `ps -f` command displays a **detailed list** of processes owned by the current user, including:

- `UID` – User ID
- `PID` – Process ID
- `PPID` – Parent Process ID
- `C` – CPU usage
- `STIME` – Start time of the process
- `TTY` – Terminal associated with the process
- `TIME` – CPU time consumed
- `CMD` – Command that started the process

### 📌 Example Output:

```bash
omkar@LAPTOP-4UCI9HKV:~$ ps -f
UID     PID   PPID  C STIME TTY      TIME     CMD
omkar   316   315   0 16:26 pts/0    00:00:00 -bash
omkar   498   316   0 16:34 pts/0    00:00:00 ps -f

Explanation:
PID 316: This is the main bash shell session (child of PPID 315)

PID 498: This is the ps -f command executed inside that shell

pstree -p – Tree View of Process Hierarchy (with PIDs)
The pstree -p command shows a hierarchical tree of processes with their PIDs, making it easier to visualize parent-child relationships.

Sample-output:
systemd(1)
 ├─ init-systemd(Ub(2)
 │   ├─ SessionLeader(314)
 │   │   └─ Relay(316)(315)
 │   │       └─ bash(316)
 │   │           └─ pstree(500)
 │   ├─ SessionLeader(440)
 │   │   └─ Relay(446)(441)
 │   │       └─ bash(446)
 │   └─ login(317)
 │       └─ bash(412)
 ├─ redis-server(199)
 ├─ rsyslogd(200)
 ├─ systemd-logind(203)
 ├─ unattended-upgr(238)
Explanation:
systemd(1): The root process in the system (first process after boot)

init-systemd(Ub(2): Parent for WSL sessions

bash(316): Main shell session for the user

pstree(500): Child process (pstree command) of bash(316)

bash(446): Another shell session in a second terminal

bash(412): Another shell started through login(317)

redis-server, rsyslogd, etc.: Background system services

Key Takeaways
Use ps -f to see detailed info about your current session's processes.

Use pstree -p to visualize process relationships and hierarchy.

Each terminal or login session spawns a new shell process (bash), and commands like pstree, ps, etc., are executed as child processes.