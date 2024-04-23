# E6K CyberCommand Capture The Flag Recap

## Our mindset going to the CTF

- Curious
- Worried that it might be too difficult 
- add things and let's format a mini text later

## At the CTF

### What was asked ?

### What are tools that can help on a CTF ?

![Kali](/Assets/kali.jpg) ![Parrot](/Assets/parrot.jpg) ![Black Arch](/Assets/blackarch.png) ![Tools](/Assets/tools.jpg)

- Nmap  : Scan and map networks, identify hosts and discover services and vulnerabilities in those hosts.
- MetaSploit : Vulnerability scanning, exploit development and payload creation.
- BurpSuite : Web application security testing, identify and exploit vulnerabilities in web applications, analyse and manipulate web application traffic.
- JohnTheRipper : Offline password cracking tool, dictionnary attacks, brute force and rainbow table attacks.
- Hydra : Online password cracking tool, dictionnary attacks, brute force and rainbow table attacks. Works with various protocols such as FTP, SSH, Telnet, HTTP, ... 
- Aircrack-ng : Auditing and cracking network wireless passwords and monitoring wireless network traffic.
- WireShark : Network protocol analyser, capture and view traffic over a network, decode and analyse packets, diagnose and solve network problems.
- HashCat : Password cracking tool, dictionnary attacks, brute force and mask attacks. It support many hash types, including MD5, SHA-1, SHA-256, SHA-512, ...

## Examples

### Rubber Ducky

One flag consisted of setting up a Raspberry Pi Pico as a rubber ducky usb driver to steal a flag on a cisco machine. 

#### So what is a rubber ducky ? 
![Rubber Ducky](/Assets/ducky.png)

A rubber ducky is  a small USB device that looks like an ordinary USB flash drive but behaves like a keyboard when plugged into a computer. It's essentially a keystroke injection tool.

- Automated Script Execution
- Password Theft 
- Physical Access Attacks

#### You can make it for cheap:

![Cheaper Rubber Ducky](/Assets/pico.png)

- https://github.com/dbisu/pico-ducky
- https://workbook.securityboat.net/hardware-security/raspberry-pi/projects/usb-rubber-ducky-using-raspberry-pi-pico

## Web Challenges-  Finding the Flag in Source Code

### Overview

In this web challenge, the goal was to locate the flag on the website `https://redsystem.io/` without using brute force or fuzzing techniques. 

The challenge included inspecting various elements of the website to uncover hidden or less obvious areas where the flag might be stored.

## Methodology

### Initial Steps

1. **View Page Source:**
   - Accessed by pressing `Ctrl+U`.
   - This action reveals the raw HTML content of the website.

2. **Developer Tools:**
   - Accessed by pressing `Ctrl+Shift+I`.
   - Used to inspect elements, linked CSS, and script files.
   - Networking tab explored to check for fetch requests that load dynamic data.
   - Resources and storage explored for any hidden data.

### Additional Checks

3. **Robots.txt:**
   - Located at `https://redsystem.io/robots.txt`.
   - Used to determine which areas of the website web crawlers are restricted from accessing. This file sometimes contains paths that are not directly linked from the website, which might hold sensitive information.

4. **Sitemap:**
   - Accessed through `https://redsystem.io/sitemap.xml`.
   - Sitemaps provide a quick way to find all the pages on a website and are crucial for locating resources that might not be obvious from the homepage or other linked pages.

    ![alt text](/Assets/sitemap.png) 

### Outcome

- After navigating through multiple layers, the flag was finally located deep in a script file.
- The process required not only a keen eye on the surface-level elements but also a deeper investigation into the structure and requests made by the web application.


### Conclusion

This challenge highlighted the importance of thorough inspection of all accessible web resources, not just those that are immediately visible. Tools like the page source viewer and developer tools were invaluable in dissecting the website's structure and ultimately led to the successful retrieval of the flag.

### Flags Found

- Two flags were discovered during this challenge, detailed exploration and strategic thinking were key to uncovering them in hidden parts of the website's structure.


## Lock - Picking

## John The Ripper

## Conclusion 

### What did we learn ? 

- Prepare
- Organise
- Specialise
- Don't hesitate to use any tool
- Take the train

### Sabotaging


### REDsystem & CyberCommand / La Défense