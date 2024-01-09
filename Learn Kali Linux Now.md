# Learn Kali Linux Now

## What is Linux

Linux is a powerful and flexible family of operating systems that are free to use and share. It was created by a person named Linus Torvalds in 1991. What’s cool is that anyone can see how the 
system works because its source code is open for everyone to explore and modify. This openness encourages people from all over the world to work together and make Linux better and better. Since its beginning, Linux has grown into a stable and safe system used in many different things, 
like computers, smartphones, and big supercomputers. It’s known for being efficient, meaning it can do a lot of tasks quickly, and it’s also cost-effective, which means it doesn’t cost a lot to use. Lots of people love Linux, and they’re part of a big community where they share ideas and help each other out. As technology keeps moving forward, Linux will keep evolving and staying important in the world of computers.

### Linux Distribution

Linux distribution  is an operating system that is made up of a collection of software based on Linux kernel or you can say distribution contains the Linux kernel and supporting libraries and software. And you can get Linux based operating system by downloading one of the Linux distributions and
 these distributions are available for different types of devices like embedded devices, personal computers, etc. Around **600 + Linux Distributions** are available and some of the popular Linux distributions are:

- MX Linux
- Manjaro
- Linux Mint
- elementary
- Ubuntu
- Debian
- Solus
- Fedora
- openSUSE
- Deepin
1. **Kernel:** Kernel is the core of the Linux based operating system. It virtualizes the common hardware resources of the computer to provide each process with its virtual resources. This makes the process seem as if it is the sole process running on the machine. The kernel is also responsible for preventing and mitigating conflicts between different processes.
**Different types of the kernel are:**
    - Monolithic Kernel
    - Hybrid kernels
    - Exo kernels
    - Micro kernels
2. **System Library:**Linux uses system libraries, also known as shared libraries, to implement various functionalities of the operating system. These libraries contain pre-written code that applications can use to perform specific tasks. By using these libraries, developers can save time and effort, as they don’t need to write the same code repeatedly. System libraries act as an interface between applications and the kernel, providing a standardized and efficient way for applications to interact with the underlying system.
3. **Shell:**The shell is the user interface of the Linux Operating System. It allows users to interact
with the system by entering commands, which the shell interprets and executes. The shell serves as a bridge between the user and the kernel, forwarding the user’s requests to the kernel for processing. It provides a convenient way for users to perform various tasks, such as running programs, managing files, and configuring the system.
4. **Hardware Layer:** The hardware layer encompasses all the physical components of the computer, such as RAM (Random Access Memory), HDD (Hard Disk Drive), CPU (Central
Processing Unit), and input/output devices. This layer is responsible for interacting with the Linux Operating System and providing the necessary resources for the system and applications to function properly. The Linux kernel and system libraries enable communication and control over these hardware components, ensuring that they work harmoniously together.
5. **System Utility:** System utilities are essential tools and programs provided by the Linux
Operating System to manage and configure various aspects of the system. These utilities perform tasks such as installing software, configuring network settings, monitoring system performance, managing users and permissions, and much more. System utilities simplify system administration tasks, making it easier for users to maintain their Linux systems efficiently.

## Kali Linux Basics for Penetration Testing Career

---

Note: To get help or understand tools or commands, use `-h` or `--help` along with the command to get verbose help output if available. There is also the `man` command for more descriptive output.

### Kali Linux File System

The Linux file system is a hierarchical file system that resembles a tree with branches.

- `/`: The root location of the file system. All files and folders can be found in this location for running and configuration purposes.
- `/root`: The home directory of the root user.
- `/bin`: Contains essential command binaries. It is a critical directory in the file system and must exist in the root directory.
- `/boot`: Contains files required to boot the system.
- `/dev`: Contains device files.
- `/etc`: Contains system-wide configuration files.
- `/home`: The home directory for users.
- `/lib`: Contains libraries needed by the essential binaries in the `/bin` directory.
- `/media`: Used as the mount point for removable media.
- `/mnt`: Used as the mount point for temporarily mounted file systems.
- `/opt`: Contains add-on application software packages.
- `/proc`: A pseudo-file system that contains kernel and process information as files.
- `/root`: The home directory for the root user.
- `/run`: Contains system information data describing the system since it was booted.
- `/sbin`: Contains essential system administration binaries.
- `/srv`: Contains data for services provided by the system.
- `/sys`: A pseudo-file system used to export kernel objects.
- `/tmp`: Used to store temporary files.
- `/usr`: The second major section of the file system, containing the majority of user utilities and applications.
- `/var`: The third major section of the file system, containing variable data files.

---

### General Commands

To change the directory through the command line, use:

`cd`: Change directory

`cd ..` To go back one level or back one directory

`../../` To go back more than one level or back more than one directory

`pwd`: (Present working directory) To get your present location in the file system, use:

`ifconfig` To see network configuration, use:

`whoami` To see who you are on the system, use:

`ls` To see the content of a directory or list items in a directory, use:

Use `ls -l` to get a long list output and hidden files that start with a dot, such as `.ssh`.

`mkdir`: Create a new directory.

`rmdir`: Remove an empty directory.

`cp`: Copy files or directories.

`mv`: Move or rename files or directories.

`rm`: Remove files or directories.

`touch`: Create an empty file or update the timestamp of an existing file.

`cat`: View the contents of a file.

`less`: View the contents of a file interactively.

`sed` : modifies lines from the specified File parameter according to an edit script and writes them to standard output.

### Finding Something

Use `locate` command to find any directory or files on the system.

To find executable binaries Use `whereis` such as `whereis nmap`

To find Location of binaries in PATH variable use `which`  ,eg `which nmap` 

`Find` The find command is more accurate to find something. It is an advance tool to find

example: `find / -type f -name hello`

### File Permissions

Start of Permission

- `-` : If - is present at first means it is regular file.
- `d` : if d is present at first means it is directory.

In Linux, each file and directory has permissions that determine who can read, write, or execute the file. The permissions are represented by a combination of letters and symbols. Here is an overview of the file permission symbols:

- `r`: Read permission. Users with read permission can view the contents of the file.
- `w`: Write permission. Users with write permission can modify the contents of the file.
- `x`: Execute permission. Users with execute permission can run the file if it is a program or script.

The file permissions are displayed as a series of 10 symbols. The first symbol represents the file type, while the next three symbols represent the owner's permissions, followed by the group's permissions, and finally, the permissions for other users.

For example, if a file has the permissions `**rw-r--r--**`, it means that the owner can read and write the file, while the group and other users can only read the file.

File permissions can be modified using the `**chmod**` command. For example, to give read, write, and execute permissions to the owner of a file, you can use the following command:

`chmod u+rwx <file-name>`

Replace `<file-name>` with the name of the file you want to modify.

**When Linux file permissions are represented by numbers, it's called numeric mode.**

- `r (read): **4**`
- `w (write): **2**`
- `x (execute): **1**`

In the permission value 744, the first digit corresponds to the user, the second digit to the group, and the third digit to others. By adding up the value of each user classification, you can find the file 
permissions.

For example, a file might have read, write, and execute permissions for its owner, and only read permission for all other users. That looks like this:

- Owner: rwx = `4+2+1 = **7**`
- Group: r-- = `4+0+0 = **4**`
- Others: r-- = `4+0+0 = **4**`

by byte prospective:

0000 = 0

0001 = 1 → 1 is 1 at 1 place

0011 = 3 → 11 is 1 and 2 at places = 1 +2 = 3

0111 =  7  111 is 1 and 2 and 3 at places = 1 +2 + 4 = 7

rwx
001 → only execute

[reference](https://ostechnix.com/linux-file-and-directory-permissions/)

**Modify permissions and users**

`sudo chown user-name file or floder-name`  : change user of file or folder  

`sudo chgrp group-name file or floder-name`  : change group of file or folder  

`sudo chmod u+rw file or floder-name`: give user permission as read and write to file or folder

`sudo chmod g+rw file or floder-name` : give group permission as read and write to file or folder

`sudo chmod o+rw file or floder-name` : give others permission as read and write to file or folder

**Note**: here + is for add permission and - for remove permission.

### Package Management

One of the advantages of using Linux is the ease of managing software packages. Linux distributions typically provide package managers to install, update, and remove software packages.

Here are some commonly used package managers in Linux:

- `apt`: Advanced Package Tool. Used by Debian-based distributions such as Ubuntu.
    - `apt install package-namednf`: Dandified YUM. Used by Fedora and Red Hat-based distributions.
- `pacman`: Package Manager. Used by Arch Linux and its derivatives.
    - `pacman -S *package_name*`
- `zypper`: Package Manager. Used by openSUSE.
- `synaptic` : Gnu(graphical user interface)  package manager

To install a package using the package manager, you can use the following command:

`sudo apt install <package-name>`

Replace `<package-name>` with the name of the package you want to install.

To update all installed packages on your system, you can use the following command:

`sudo apt update && sudo apt upgrade`

This will update the package lists and upgrade all installed packages to their latest versions.

### Network Configuration

Linux provides various tools to configure and manage network settings. Here are some useful commands:

- `ifconfig`: Display or configure network interfaces.
    - `ifconfig eth0 IP` Get a Static ip address.
- `iwconfig` : Display or configure wireless interfaces.
- `ping`: Send ICMP echo requests to a specified network host.
- `netstat`: Display network connections, routing tables, and network interface statistics.
- `ssh`: Connect to a remote server using the Secure Shell (SSH) protocol.
- `scp`: Securely copy files between hosts using SSH.
- `wget`: Download files from the web.
- `curl`: Transfer data to or from servers using various protocols.
- `dhclient eth0` : Get dynamic ip address.
- `/etc/resolv.conf` : This is a dns configuration file.

Tese commands can help you troubleshoot network issues, configure network interfaces, and perform various network-related tasks. For example, you can use `ifconfig` to view or configure network interfaces, `ping` to check the connectivity to a network host, and `ssh` to establish a secure connection to a remote server.

Please note that the above information is just a brief overview, and there are many more commands and concepts to explore in Linux. Experimenting with different commands and exploring the Linux documentation will help you deepen your understanding of the operating system.

### System Utilities

Linux provides a wide range of system utilities that help manage and configure various aspects of the system. These utilities simplify system administration tasks and make it easier to maintain a Linux system efficiently. Here are some commonly used system utilities:

- `top`: Monitor system resource usage, including CPU, memory, and processes.
- `df`: Display disk space usage on file systems.
- `du`: Estimate file and directory space usage.
- `ps`: Display information about active processes.
    - `ps aux` : Display all processes.
- `kill`: Terminate processes or send signals to processes.
- `useradd`: Create a new user account.
- `usermod`: Modify user account settings.
- `passwd`: Change user passwords.
- `ifconfig`: Display or configure network interfaces.
- `iptables`: Configure firewall rules.
- `crontab`: Schedule and manage cron jobs.
- `echo PATH` : To find which directories your shell is set to check for executable files.
- `printevn` : List pre-defined PATH Variables.
- `grep` : grep is a filter that is used to search for lines matching a specified pattern and print the matching lines to standard output.

### Download and Install Software

`sudo apt-cache search package-name` : Check for package in apt cache memory.

`apt install package-name` : Install software if available in cache.

`apt update` : It will update apt-cache.

`apt remove package-name`: It will remove packages.

`apt purge package-name` : It will remove configuration files for that particular package.

`/etc/apt/sources.list` : Source file which system look for packages.

`git clone url` : Used for download custom packages or tools from GitHub.