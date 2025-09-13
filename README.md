# learning_cyber_pwn
In this repository, I will be documenting my learning journey of PWN College's contents. 

# September 13th, 2025 

Just learned about file globbing. I learned that * is a wildcard for a non-especified number of characters, and it can be any of them (including nothing), while ? substitutes only one character. Some interesting things that tricked me were:

1) The difference between:

echo "Look: myfile/file_[123]"
vs 
echo Look: myfile/file_[123]

In the first one, the brackets are not expanded, but they are in the second one.

2) If you only write the name of a path and enters it on the terminal and some files don't show up, it meand that these files were not executable. 

Also, a really great tip from the plataform regarded the use of ! and ^. They clarified that the position of ! relative to the brackets (exclusive globbing) matters, which doesn't happen with ^ - however, older shells might not recognize the latter.

Lastly, I did the first challenge of the module "Processes and Jobs". That was my first introduction to this topic, and the challenge, yet simple, got me thinking about the beauty of the way computers perform tasks. 