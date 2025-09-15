# September 13th, 2025 

Just learned about file globbing. I learned that * is a wildcard for a non-especified number of characters, and it can be any of them (including nothing), while ? substitutes only one character. Some interesting things that tricked me were:

1) The difference between:

echo "Look: myfile/file_[123]"
vs 
echo Look: myfile/file_[123]

In the first one, the brackets are not expanded, but they are in the second one.

2) If you only write the name of a path and enters it on the terminal and some files don't show up, it meand that these files were not executable. 

Also, a really great tip from the plataform regarded the use of ! and ^. They clarified that the position of ! relative to the brackets (exclusive globbing) matters, which doesn't happen with ^ - however, older shells might not recognize the latter.

Lastly, I initiated the Processes and Jobs module and did its first challenge, Listing Processes. That was my first contact with the topic. It was really beautiful to see the processes list. That's some exciting journey! 

# September 15th, 2025

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
