# TELEFONIKA Lab

This lab tests the student's ability to detect bad practices in web development and exploit credential exposure on a landing page. Through this exercise, students will learn to:

- Analyze HTML source code for security flaws.
- Detect improperly exposed credentials.
- Connect via SSH using discovered credentials.
- Access a flag without the need for privilege escalation.

## Machine Specifications 🖥️

- **System:** Ubuntu Server (or Debian without GUI)
- **Web Server:** Apache or Nginx
- **Site Path:** `/var/www/html/index.html`
- **Vulnerable Content:** Form with hidden HTML comment:

```html
<!-- Boss, I will put the credentials right here so you can test: larry:TELEFONIKA25 -->
```

- **User:** `larry`  
- **Password:** `TELEFONIKA25`  
- **Flag:** `/home/larry/flag.txt`  
- **Flag Content:**  
    `4GEEKS{D0nt_3XP0S3_TH3_cR3d3nt14ls_L1K3_TH15!!!}`  
- **Note:** `larry` does not have `sudo` permissions.

### Machine Credentials

```bash
servername: telefonika-lab
username: student
password: 4geeks-lab
```

## Expected Steps for the Student

1. **Perform network reconnaissance to identify the machine.**
     - Use tools like `nmap`, `netdiscover`, or `arp-scan`.
     - Identify an IP with **80 (HTTP)** and **22 (SSH)** ports open.

2. **Access the website from the browser.**
     - Enter the discovered IP in the browser to load the TELEFONIKA landing page.

3. **Review the website's source code.**
     - Identify an HTML comment exposing a username and password.

4. **Connect via SSH using the discovered credentials.**
     - Log in as `larry` using:
         ```bash
         ssh larry@<IP>
         ```
         Password: `TELEFONIKA25`

5. **Find and read the flag.**
     - Located in `larry`'s home directory as `flag.txt`:
         ```bash
         cat ~/flag.txt
         ```
