# Telefonika - CTF machine for vulnerability exposed Code Analysis

In this capture the flag lab, you will analyze a seemingly simple web page, discover improperly leaked credentials, and access a system via SSH to retrieve a flag. In this lab, you will learn:

- HTML source code analysis
- Detection of poor web development practices
- Remote access via SSH
- Reading flags on Linux systems


<how-to-start>
   
## 🌱 How to Start This Lab

Follow these instructions to get started:

1. **Download the virtual machine** from this link:

<onlyfor withbanner="true" permission="get_private_link">
   
```url
  https://storage.googleapis.com/cybersecurity-machines/telefonika-lab.ova
```

</onlyfor>

2. **Import the machine** into your preferred virtualization software (VirtualBox, VMware, etc.).
3. Once the machine is running, you can start the lab!

</how-to-start>


## 📄 Instructions

You are facing the website of an internet and telephony service company called **TELEFONIKA**. Your task is to analyze how the page is built and discover if there are any exploitable vulnerabilities.


1. **Discover the IP address of the TELEFONIKA machine.**
   - The machine is connected to the same network as you, but its IP has not been provided.
   - Use tools like `nmap` to scan the network.

2. **Access the website hosted on the server.**
   - Open your browser and visit the assigned IP.
   - Observe the content of the form.

3. **Inspect the source code.**
   - Are there any comments that shouldn't be there?
   - Pay attention to potential information leaks.

4. **Use the information found to connect via SSH.**
   - If you find credentials, try accessing the system.
   - The goal is to log in as a real system user.

5. **Find the flag.**
   - Check the personal directory of the user you managed to access.
   - Privilege escalation is not required.



**Remember:** sometimes the keys are not hidden... just poorly placed.

Happy hacking!
