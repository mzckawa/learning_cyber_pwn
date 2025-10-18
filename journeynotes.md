## September 13th, 2025 

Just learned about file globbing. I learned that * is a wildcard for a non-especified number of characters, and it can be any of them (including nothing), while ? substitutes only one character. Some interesting things that tricked me were:

1) The difference between:

echo "Look: myfile/file_[123]"
vs 
echo Look: myfile/file_[123]

In the first one, the brackets are not expanded, but they are in the second one.

2) If you only write the name of a path and enters it on the terminal and some files don't show up, it meand that these files were not executable. 

Also, a really great tip from the plataform regarded the use of ! and ^. They clarified that the position of ! relative to the brackets (exclusive globbing) matters, which doesn't happen with ^ - however, older shells might not recognize the latter.

Lastly, I initiated the Processes and Jobs module and did its first challenge, Listing Processes. That was my first contact with the topic. It was really beautiful to see the processes list. That's some exciting journey! 

## September 15th, 2025

In the "killing processes" module, I learned that the pgrep command allows makes the terminal show only the PID number of the process that you're looking for. The argument -f allows you to search for the PID using the path name, not the comm, and the argument -a allows you to see the string that the pregp command matched with. Also, I learned that "comm" means "command name" and, in Linux, is a short name - not longer than 15 characters - that the kernel gives to the process. 

I learned that "listening to a keybinding" refers to the way a keybinding triggers a certain command on the machine. The software is "listening" to the keyboard inputs all the time, and when some keys are pressed, it performs specific tasks. 

Through the "Killing Misbehaving Process" challenge, I learned that:

-> You use PID, not PPID to kill the process.
-> You can only kill a process if you "own" it. 
-> "&" makes a command run in the background, so your prompt is free to use. 

Understanding deeply this challenge was a bit tricky for me and I feel like a need some time to actually cement the topic, but it was nice to review my knowledge about FIFOs and how we need to unblock both their writing and reading endings. 

In the "Suspending Processes" challenge, I learned about the keybinding ctrl + z.

In the "Backgrounding Processes", I learned that the "-o" argument in the ps command allows the specified informations ("info1,info2,info3") to be displayed. 
Furthermore, about the STAT column, I learned that S means that the process is "sleeping" while waiting for input; + means that it is on the foreground, and R means that is is activelly running. 
Also, I learned that when "bg" is passed without any arguments, the shell understands that you're referring to the last suspended command. However, if you need to specify it, you can pass an argument such as "%[job number]" or "%[command prefix]". 
On top of that, I learned that when you write a command on the prompt and does not wait for another prompt line to appear before writing the next command, your are interacting with the first command, not with the shell, which may or may not make sense! 

In the "Process Exit Codes" challenge, I learned that we type $? because this is how the shell is going to recognize that we want the error code of the last command executed. If we type echo ?, the shell will look for one-charachter file names and and, if it doesn't match anything, it will print "?".

## September 23th, 2025. 

Today, I learned that operating systems have many "users" and that they don't necessarily refer to real people using the machine. Also, I learned about the importance of the root user, and solved a challenge that used an old way off gaining root privileges, the "su" command. 

## October 15th, 2025.

Today, I learned abou the difference between how su and sudo give root privileges, and finished the module "Untangling users" (Linux Luminarium).

## October 17th, 2025. 

Today, I started learning about Access Control, and watched the "Access Control: Introduction" video, the first one from the Perceiving Permissions module. I learned the difference between authorization (what can you do) and autentication (who are you), reflected about risks, that is, the probability of something bad happening and about how the access control mechanisms may prevent people from being found guilty for something insecure they didn't do on purpose.

## October 18th, 2025.

Today, I watched the video "Access Control: Modeling Access Control", also from the "Perceiving Permissions" module. I learned the concepts os subjects (things in the system that can act), objects (things in the system that are acted upon) and rights (what the subjects can do to the objects). What is considered subject or object (or both) depends on each system, and a subject may have different rights upon different objects. 
Also, an interesting thing to reflect upon was that, for the system, we are not the subject; rather, subjects are processes, and files are objects.
At this module, we are going to explore the following rights: read, write, execute, append (it only allows you to add things to the file, but not to change anything that came before it, which may help prevent risks), own (allows you to give rights to other processes for that object). 
At the end, some of the benefits and drawbacks of Access Control Matrix Models were discussed. 
