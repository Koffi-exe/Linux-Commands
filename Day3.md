# Day 3: Process and User Management

## 1. Check Current User

```bash
whoami
```

> Gives the details of the current user

---

## 2. Check User ID Information

```bash
id
```

> Example output:
```bash
uid=1000(ubuntu) gid=1000(ubuntu) groups=1000(ubuntu),4(adm),24(cdrom),27(sudo),30(dip),105(lxd)
```

---

## 3. Adding a New User

```bash
sudo adduser koffi
```

> System messages:
```bash
info: Adding user `koffi' ...
info: Selecting UID/GID from range 1000 to 59999 ...
info: Adding new group `koffi` (1001) ...
info: Adding new user `koffi` (1001) with group `koffi (1001)` ...
warn: The home directory `/home/koffi` already exists. Not touching this directory.
```

> Password prompts:
- New password:
- Retype new password:

```bash
passwd: password updated successfully
```

> User info setup:
```bash
Changing the user information for koffi
Enter the new value, or press ENTER for the default
```

User details:
- Full Name []: Koffi K  
- Room Number []: 12  
- Work Phone []: 8085775955  
- Home Phone []: 8085775955  
- Other []:

> *When typing the password, the cursor will not move. Don't panic — it is not stuck.*

---

## 4. User Management Commands

- **Switching to another user:**
  ```bash
  su - <username>
  ```
  Then type the password.

- **Make a user a superuser:**
  ```bash
  sudo usermod -aG sudo koffi
  ```

- **Change a user's password:**
  ```bash
  sudo passwd <username>
  ```

- **Delete a user:**
  ```bash
  sudo deluser <username>
  ```

---

## 5. Process and Resource Management

- **CPU and Memory Usage:**
  ```bash
  top
  ```

- **Check Running Processes:**
  ```bash
  ps
  ```

- **Create a Process:**
  ```bash
  sleep 300 && echo "Hello"
  ```
  > This command will create a process that sleeps for 300 seconds and then prints "Hello".

- **Kill a Process:**
  ```bash
  ps             # Use this to find the process ID
  kill <pid>     # Standard kill
  kill -9 <pid>  # Forcefully removes the process
  ```
