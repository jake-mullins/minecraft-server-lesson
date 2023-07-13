# Minecraft Lesson

This is a lesson that teaches basic operating system and networking skills using a Minecraft server on a Linux machine.

Setting up and connecting to a Minecraft server on a Linux machine takes many different skills including:
- Basic networking
- Basic OS knowledge
- Basic Linux command line

And most importantly:

- Troubleshooting using online resources.

--- 

General order of topics:
- What is an OS?
- Why use Linux instead of Windows?
- What is Ubuntu vs Linux?
- Distribution pretty much equals Operating System 
- Basic Linux command line (ls, cd, sudo, chmod/chown).
- How do we get answers to our questions using the internet?
- What is a server?
- Download minecraft server binary.
- Download tools to run binary (jre).
- Run server binary.
- Basic networking (Local/Public IPs and ports.
- Nmap service scan on port 25565 on host running the server.
- Connect to the server using the minecraft client.

The instructions below are intentionally left vague without links so that students are encouraged to find their own solutions online.

Instructions for Students:

1. Start downloading the latest Minecraft server jarfile.
2. While you're at it, start downloading the Minecraft client, including the latest version.
3. 

Annotated Instructions for Instructors:

1. Start downloading the latest Minecraft server jarfile. [Server download](https://www.minecraft.net/en-us/download/server)
2. While you're at it, start downloading the Minecraft client, including the latest version. [Client download](https://www.minecraft.net/en-us/download).
3. Press the window key/home button and search for the Terminal.
4. Make sure that the terminal looks something like:
```
<username>@<hostname>:~$
```
*Explain what a terminal is and how it differs from a GUI*

5. Create a directory called ```minecraft``` using the command
```
mkdir minecraft
```
- *What is a filesystem?*
- *Directories vs files*

5. Run
```
cd Downloads
```
- *Current working dir*
- *cd command*

and look at the contents of ```minecraft``` by running
```
ls
```
- *ls command*

6. Move the ```server.jar``` file to the minecraft folder using
```
mv ./server.jar ../Downloads/server.jar
```
- *Relative paths vs absolute paths*
- *Maybe cp vs mv and how mv is for renaming too*

7. A ```.jar``` file is a program that can be run by running the following command. 
```
java -jar <program>.jar
```
*Meant to fail*

If you got something like 
```
-bash: java: command not found
```
That's completely fine! It just means we have to get java on your computer, which means installing the default JRE (Java Runtime Environment). When you're dealing with Java, you'll see a lot of acronyms starting ```j```. Don't worry about learning those for now.
- *Might be a good idea to ask if a .jar looks like a regular file, directory, or executable*

8. Just like most operating systems, each Linux distribution comes with a standardized way of distributing new software. For Windows, it's the Windows store. For MacOS and your iPhone it's the Apple App Store. For Linux, this is called a **Package Manager**. For the distribution we're using, this package manager is called ```apt``` or **A**dvanced **P**ackage **T**ool.

If we want to learn more information about ```apt```, a could place to look is the manual pages. These can be accessed using:

```
man apt
```

There's a lot of confusing terms, so instead, let's just look up how to install a package using ```apt``` on the internet. We're not going to give you the command here, so you'll have to figure it out yourself.

Don't run the command yet.

- *sudo apt install <package>*

9. But wait! What is that ```sudo``` part of the command? In Linux, there are a lot of actions that require elevated privileges to make sure that users on the system don't do anything they're not supposed to do. Look at your command line prompt. The format of the prompt is

```
<user>@<computer name>:~$
```

-*Ask "What is your user name?" to students*
-*Ask "Why would it be useful to restrict access to certain actions?"*

These elevated privileges are called **root privileges**. With root privileges, you gain access to the ```sudo``` command. ```sudo``` means **S**uper **U**ser **DO**, and for one command only, makes the computer think that you are a super user, or a user that can do anything to the computer.

10. Run the command to install the package ```default-jre```.

11. Run 
```
java -Xmx1024M -Xms1024M -jar minecraft_server.1.20.1.jar nogui 
```

to start the server. We found this command on the download page for the server. It will run for about and ask you to agree to a EULA before continuing. If you already know terminal based text editors, you can use that. If you don't, use the file explorer to open the ```EULA.txt``` in the ```minecraft``` folder. 

Change ```eula=false``` to ```eula=true```. If it automatically opened LibreOffice, a software similar to Microsoft Word, make sure to click ```Use Text Format```, not ```Use ODF Format```.

12. Use the up arrow in the terminal to rerun the command, or copy and paste it again from the website.

After a while, you should see it start out map generation information
