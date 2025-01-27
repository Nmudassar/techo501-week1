# Linux Command Cheat Sheet

A quick reference guide for commonly used Linux commands.

---

## 1. `ls`

- **Purpose:** Lists files and directories in the current location.
- **Example:**
  ```bash
  ls
  ```

---

## 2. `ls -a`

- **Purpose:** Lists all files, including hidden ones (those starting with `.`).
- **Example:**
  ```bash
  ls -a
  ```

---

## 3. `ls -l`

- **Purpose:** Shows detailed file info, including permissions, owner, size, and timestamp.
- **Example:**
  ```bash
  ls -l
  ```

---

## 4. `ls -al`

- **Purpose:** Combines `-a` and `-l` to list **all files** in **detailed format**.
- **Example:**
  ```bash
  ls -al
  ```

---

## 5. `cd ..`

- **Purpose:** Moves up one directory.
- **Example:**
  ```bash
  cd ..
  ```

---

## 6. `pwd`

- **Purpose:** Prints the current working directory.
- **Example:**
  ```bash
  pwd
  ```

---

## 7. `curl <URL>`

- **Purpose:** Downloads content from a URL.
- **Example:**
  ```bash
  curl https://example.com
  ```

---

## 8. `curl <URL> --output <filename>`

- **Purpose:** Downloads data and saves it to a file.
- **Example:**
  ```bash
  curl https://example.com/image.jpg --output myimage.jpg
  ```

---

## 9. `file <filename>`

- **Purpose:** Tells you the file type.
- **Example:**
  ```bash
  file myfile.txt
  ```

---

## 10. `mv <source> <destination>`

- **Purpose:** Moves or renames a file.
- **Examples:**
  - Rename a file:
    ```bash
    mv oldname.txt newname.txt
    ```
  - Move a file:
    ```bash
    mv myfile.txt /home/user/docs/
    ```

---

## 11. `cp <source> <destination>`

- **Purpose:** Copies a file.
- **Example:**
  ```bash
  cp myfile.txt backupfile.txt
  ```

---

## 12. `rm <filename>`

- **Purpose:** Deletes a file.
- **Example:**
  ```bash
  rm myfile.txt
  ```

---

## 13. `rm -r <directory>`

- **Purpose:** Deletes a directory and all its contents.
- **Example:**
  ```bash
  rm -r mydirectory
  ```

---

## 14. `mkdir <directory>`

- **Purpose:** Creates a new directory.
- **Example:**
  ```bash
  mkdir newfolder
  ```

---

## 15. `touch <filename>`

- **Purpose:** Creates an empty file or updates its timestamp.
- **Example:**
  ```bash
  touch newfile.txt
  ```

---

## 16. `cat <filename>`

- **Purpose:** Displays the contents of a file.
- **Example:**
  ```bash
  cat myfile.txt
  ```

---

## 17. `nano <filename>`

- **Purpose:** Opens a file in the Nano text editor.
- **Example:**
  ```bash
  nano myfile.txt
  ```

---

## 18. `head -n <number> <filename>`

- **Purpose:** Displays the first `n` lines of a file.
- **Example:**
  ```bash
  head -2 myfile.txt
  ```

---

## 19. `tail -n <number> <filename>`

- **Purpose:** Displays the last `n` lines of a file.
- **Example:**
  ```bash
  tail -2 myfile.txt
  ```

---

## 20. `nl <filename>`

- **Purpose:** Displays file contents with line numbers.
- **Example:**
  ```bash
  nl myfile.txt
  ```

---

## 21. `grep <pattern> <filename>`

- **Purpose:** Searches for a specific text pattern in a file.
- **Example:**
  ```bash
  grep "error" logfile.txt
  ```

---

## 22. `apt install <package>`

- **Purpose:** Installs software packages using APT.
- **Example:**
  ```bash
  sudo apt install tree
  ```

---

## 23. `tree`

- **Purpose:** Displays a directory structure as a tree.
- **Example:**
  ```bash
  tree
  ```

---

## 24. `printenv <variable>`

- **Purpose:** Shows the value of an environment variable.
- **Example:**
  ```bash
  printenv PATH
  ```

---

## 25. `export <variable>=<value>`

- **Purpose:** Sets an environment variable.
- **Example:**
  ```bash
  export MYNAME=Nadia
  ```

---

## 26. `echo <text>`

- **Purpose:** Outputs text to the terminal.
- **Example:**
  ```bash
  echo "Hello, world!"
  ```

---

## 27. `echo "<text>" >> <filename>`

- **Purpose:** Appends text to a file.
- **Example:**
  ```bash
  echo "export MYNAME=Nadia" >> ~/.bashrc
  ```

---

## 28. `source <filename>`

- **Purpose:** Applies changes from a configuration file.
- **Example:**
  ```bash
  source ~/.bashrc
  ```

---

## 29. `history`

- **Purpose:** Shows the command history.
- **Example:**
  ```bash
  history
  ```

---

## 30. `ps`

- **Purpose:** Lists active processes for the current user.
- **Example:**
  ```bash
  ps
  ```

---

## 31. `top`

- **Purpose:** Displays real-time system resource usage and active processes.
- **Example:**
  ```bash
  top
  ```

---

## 32. `sleep <seconds>`

- **Purpose:** Pauses the shell for the specified time.
- **Example:**
  ```bash
  sleep 3
  ```

---

## 33. `jobs`

- **Purpose:** Lists background jobs in the current shell.
- **Example:**
  ```bash
  jobs
  ```

---

## 34. `sudo systemctl status <service>`

- **Purpose:** Checks the status of a service (e.g., nginx, apache).
- **Example:**
  ```bash
  sudo systemctl status nginx
  ```

---

## 35. `chmod +x <filename>`

- **Purpose:** Makes a file executable.
- **Example:**
  ```bash
  chmod +x script.sh
  ```

---

## 36. `exit`

- **Purpose:** Logs out or exits the shell.
- **Example:**
  ```bash
  exit

  ```
