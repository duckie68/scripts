# Script Folder
This is my personal scripts folder.  If you find any of these useful, then have at you.

I am a writer by trade with some experience in programming.  Some stuff will be my "experienced" work, and some is going to be amateur work based upon teaching non-programmers how to use ready made programs for their own use... Yes, I am making script kiddies.

## screenplay
This script started it all.  While the big lesson in my article was how to ask the right questions - skipping the details about writing screenplays, and breaking down problems as simple data manipulation - it was helpful to provide a simple script to demonstrate how many tasks can be easily automated without a CS degree just by looking.

This script creates a boilerplate to begin an organized writing session, creating directories and files that will help the writer get started with the project.

It takes a multi-word argument as a screenplay title.

It then creates a folder named after the screenplay with spaces replaced by underscores, and a subfolder called `assets`.  It then creates a file titled `notes.md` and a screenplay file of the screenplay name (with underscores) in the fountain format.

Finally, it populates the front end matter of the fountain file with screenplay name, writer, draft date, and contact information, as well as other supplementary fields that can be filled in by the end user.

## shellscript
This had more to do with wanting to demonstrate that I can write much better code than in `screenplay` than anything else.  Also, it provides a decent front end for my next creation - an all encompassing boilerplate program for any possible project.

This particular script is built around my own personal usage, but the second commit for it will be heavily commented as well.

This script takes a single argument, the shell script name, and creates a boilerplate for a shell script in my `$HOME/.scripts/personal` directory.  The boilerplate is based upon **"Mastering UNIX Shell Scripting"**, but may change.

Upon creation of the file, it calls up **nvim** with the file in the buffer.

I did not do anything to set script permissions, so `chmod +x` will be needed to run it still.

## spreport
This is a report utility for fountain screenplay formatted scripts.

It begins by listing the number of lines per character.

Next, it will ask if you wish to save this as a report.  Answering yes will cause it to generate a `report.txt` listing all characters and the number of lines they have.  **WARNING** this will overwrite any file named `report.txt` in the directory this script is run in.

The reason it asks if you wish for a report is because of one slight vagary that I dislike in any screenplay markdown or editor.  Any character that is listed as off screen **(O.S.)** or voiceover **(V.O.)** on the character line is listed as a separate character.  Seeing this in a report makes for a good time to change those into parantheticals so you can get best use out of this script.

Next, the script asks if you wish for it to generate individual character scripts.  I have never seen this functionality in any screenplay software, and I don't know why not.  Each individual character script will produce a file with only that characters lines in it.  Though not all actors will use something like this, it can be an aid to memorization for some.  Since the character scripts are still in fountain format, they can be pretty printed in screenplay style with any parser.

# TODO:
The next logical step is to take both of these templates, and turn them into functions to be used in an all inclusive shell program that will create whatever template I want.  Again, these programs are used for teaching, and will all be heavily commented, so anyone should be able to easily create templates of their own based around file creation, data population, and directory structure.  Even going so far as opening up an entire development environment to specific standards.
