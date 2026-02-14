Here’s a practical overview of **common Linux commands** grouped by what they’re typically used for:

---

## 📁 1. File & Directory Management

| Command | Description                  | Example              |
| ------- | ---------------------------- | -------------------- |
| `ls`    | List files and directories   | `ls -la`             |
| `cd`    | Change directory             | `cd /home/user`      |
| `pwd`   | Show current directory       | `pwd`                |
| `mkdir` | Create directory             | `mkdir new_folder`   |
| `rmdir` | Remove empty directory       | `rmdir folder`       |
| `rm`    | Remove file/directory        | `rm file.txt`        |
| `rm -r` | Remove directory recursively | `rm -r folder`       |
| `cp`    | Copy files/directories       | `cp file1 file2`     |
| `mv`    | Move or rename               | `mv old.txt new.txt` |
| `touch` | Create empty file            | `touch file.txt`     |
| `file`  | Show file type               | `file test.txt`      |

---

## 📄 2. Viewing & Editing Files

| Command | Description                   | Example               |
| ------- | ----------------------------- | --------------------- |
| `cat`   | Show file content             | `cat file.txt`        |
| `less`  | View large files (scrollable) | `less file.txt`       |
| `more`  | Simple viewer                 | `more file.txt`       |
| `head`  | First lines of file           | `head -n 10 file.txt` |
| `tail`  | Last lines of file            | `tail -f logfile.log` |
| `nano`  | Simple text editor            | `nano file.txt`       |
| `vim`   | Advanced text editor          | `vim file.txt`        |

---

## 🔍 3. Searching

| Command  | Description           | Example                     |
| -------- | --------------------- | --------------------------- |
| `grep`   | Search text in files  | `grep "word" file.txt`      |
| `find`   | Search files          | `find /home -name file.txt` |
| `locate` | Fast file search      | `locate file.txt`           |
| `which`  | Find command location | `which python`              |

---

## 📊 4. System Information

| Command  | Description           | Example         |
| -------- | --------------------- | --------------- |
| `top`    | Real-time processes   | `top`           |
| `htop`   | Better process viewer | `htop`          |
| `ps`     | Show processes        | `ps aux`        |
| `df`     | Disk usage            | `df -h`         |
| `du`     | Directory size        | `du -sh folder` |
| `free`   | Memory usage          | `free -h`       |
| `uname`  | System info           | `uname -a`      |
| `whoami` | Current user          | `whoami`        |
| `uptime` | System running time   | `uptime`        |

---

## 🔐 5. Permissions & Ownership

| Command  | Description        | Example                     |
| -------- | ------------------ | --------------------------- |
| `chmod`  | Change permissions | `chmod 755 file.sh`         |
| `chown`  | Change owner       | `chown user:group file.txt` |
| `groups` | Show user groups   | `groups`                    |

---

## 🌐 6. Networking

| Command   | Description    | Example                    |
| --------- | -------------- | -------------------------- |
| `ping`    | Test network   | `ping google.com`          |
| `curl`    | Transfer data  | `curl example.com`         |
| `wget`    | Download files | `wget file_url`            |
| `ssh`     | Remote login   | `ssh user@host`            |
| `scp`     | Secure copy    | `scp file user@host:/path` |
| `ip`      | Network info   | `ip addr`                  |
| `netstat` | Network status | `netstat -tuln`            |

---

## 📦 7. Package Management (varies by distro)

### Debian/Ubuntu

```
sudo apt update
sudo apt upgrade
sudo apt install package_name
```

### RedHat/CentOS/Fedora

```
sudo dnf install package_name
sudo yum install package_name
```

---

## 🔧 8. Process Management

| Command   | Description          | Example           |
| --------- | -------------------- | ----------------- |
| `kill`    | Kill process by PID  | `kill 1234`       |
| `killall` | Kill by name         | `killall firefox` |
| `bg`      | Resume in background | `bg`              |
| `fg`      | Resume in foreground | `fg`              |
| `jobs`    | Show background jobs | `jobs`            |
| `nohup`   | Run immune to logout | `nohup command &` |

---

## 📂 9. Archives & Compression

| Command    | Description   | Example                    |
| ---------- | ------------- | -------------------------- |
| `tar`      | Archive files | `tar -cvf file.tar folder` |
| `tar -xvf` | Extract       | `tar -xvf file.tar`        |
| `gzip`     | Compress      | `gzip file`                |
| `gunzip`   | Decompress    | `gunzip file.gz`           |
| `zip`      | Zip archive   | `zip file.zip file.txt`    |
| `unzip`    | Extract zip   | `unzip file.zip`           |

---

## ⚙️ 10. Useful Shortcuts & Operators

| Symbol     | Meaning             |             |
| ---------- | ------------------- | ----------- |
| `>`        | Redirect output     |             |
| `>>`       | Append output       |             |
| `          | `                   | Pipe output |
| `&&`       | Run next if success |             |
| `;`        | Run sequentially    |             |
| `*`        | Wildcard            |             |
| `Ctrl + C` | Stop process        |             |
| `Ctrl + Z` | Suspend process     |             |
| `Ctrl + D` | Logout/EOF          |             |

Example:

```bash
ps aux | grep python
```

---

If you'd like, I can also provide:

* ✅ A **Linux command cheat sheet (printable version)**
* ✅ Commands for **beginners only**
* ✅ Commands for **DevOps / system admin**
* ✅ Commands for **programmers**
* ✅ Advanced shell usage (bash scripting, pipes, awk, sed)

Just tell me your level or purpose 😊
