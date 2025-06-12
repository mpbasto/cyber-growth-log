# 🐧 Linux Fundamentals Cheat Sheet

## 📁 File System Hierarchy

| Path       | Purpose                 |
| ---------- | ----------------------- |
| `/home`    | User directories        |
| `/etc`     | System config files     |
| `/var/log` | Log files               |
| `/usr`     | User-installed software |
| `/bin`     | Essential binaries      |
| `/dev`     | Devices                 |

---

## 🔍 Navigation & File Management

| Command          | Description                   |
| ---------------- | ----------------------------- |
| `pwd`            | Print current directory       |
| `cd <path>`      | Change directory              |
| `ls -la`         | List files (long, hidden)     |
| `touch <file>`   | Create empty file             |
| `mkdir <dir>`    | Create directory              |
| `cp <src> <dst>` | Copy file                     |
| `mv <src> <dst>` | Move/rename file              |
| `rm -r <dir>`    | Remove directory and contents |

---

## 🔐 Permissions

**Format Example:** `-rwxr-xr--`  
This shows:

- A regular file (`-`)
- **Owner** has read (r), write (w), execute (x)
- **Group** has read and execute
- **Others** have only read

| Symbol | What It Means                      |
| ------ | ---------------------------------- |
| `r`    | Read permission                    |
| `w`    | Write permission                   |
| `x`    | Execute permission (run as script) |
| `-`    | No permission                      |

**Numeric Chmod Guide:**

- `r = 4`, `w = 2`, `x = 1`
- Add up for each role (Owner, Group, Others)
- Example: `chmod 755 file`
  - `7 = rwx`, `5 = r-x`, `5 = r-x`

**Useful Commands:**

- `chmod +x script.sh` → Add execute permission
- `chown user:group file` → Change owner/group
- `ls -l` → View permissions in long listing

---

## 👥 Users & Groups

| Command                   | Description       |
| ------------------------- | ----------------- |
| `whoami`                  | Current user      |
| `id`                      | UID, GID, groups  |
| `adduser <name>`          | Add new user      |
| `usermod -aG <group> <u>` | Add user to group |

---

## 🔧 Packages & Processes

| Command                     | Description                     |
| --------------------------- | ------------------------------- |
| `ps aux`                    | List all running processes      |
| `top` / `htop`              | Real-time process monitor       |
| `kill <PID>`                | End process by PID              |
| `apt update && apt upgrade` | Update packages (Debian/Ubuntu) |
| `apt install <package>`     | Install a package               |
| `dpkg -l`                   | List installed packages         |

---

## 📦 Extras

### Logs & System Files

- `/var/log/syslog` – General system messages
- `/var/log/auth.log` – Login & sudo attempts
- `/etc/passwd` – User account info
- `/etc/shadow` – Encrypted user passwords
- `/etc/group` – Group definitions

### Bash Scripting

- Start with shebang: `#!/bin/bash`
- Save script as `.sh`, make executable: `chmod +x script.sh`
- Run it: `./script.sh`

```bash
#!/bin/bash
echo "Hello, world!"
```
