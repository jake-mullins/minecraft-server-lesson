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
That's completely fine! It just means we have to get java on your computer, which means installing the default JRE (Java Runtime Environment).
- *Might be a good idea to ask if a .jar looks like a regular file, directory, or executable*

8. Just like most operating systems, each Linux distribution comes with a standardized way of 