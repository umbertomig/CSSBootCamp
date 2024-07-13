# 2022-2023 UCSD Computational Social Sciences Unix Tutorial
 
This repository has a sample set of files which students will interact with during their css tutorial.  Below are the tasks students are asked to complete.

## Tasks

*Note that Datahub has stripped the `man` pages for most of these utilities to save space, which is awful.  You can retrieve `man` pages either on your own machine, or using a site like <https://linux.die.net/man>*

1. We'll start like most academic papers, with a literature review. Look at the folder `literature`, and just using the `ls` command (and its various flags), tell me which of the files is the longest.
1. Use the `wc` command to confirm that the largest file also has the largest number of words and lines.
1. Try both `cat` and `more` to read `literature/thebrotherskaramazov.txt`, and learn quickly why you choose one over the other.
1. Let's learn a bit more about the Brothers Karamazov.  Dostoevsky often uses flies as a metaphor for evil and nastiness.  Use `egrep` to find all instances of `flies` in the text and see if this holds true.  
1. There are three Brothers (sort of), 'Alexey', 'Ivan', and 'Dmitri'.  Count the number of times each one is mentioned by name to see which is the most discussed character. You only need one command per brother.  *Hint: egrep returns one line per match*
1. This isn't a good method, given that Russian often uses diminuitive forms, so 'Alexey' is often called 'Alyosha', 'Ivan' is often 'Vanya', and 'Dmitri' is often 'Mitya'. Again using one command per brother, see how many times (e.g.) either Alexey or Alyosha is mentioned. 
	- You'll need to use `egrep` with the `|` between queries for this to work.  Use the tutorial at <https://savethevowels.org/unix> if you're not sure.
1. Dostoevsky uses the term 'apothecary' only twice in the book.  Let's look at some context. Use `egrep` with the `-C 2` flags to see two lines of context to either side of the word 'apothecary'. (This is a capital C, that's important!)
1. Time to create a poetry anthology. Create a new file called `anthology.txt` which contains the five poems in `literature`, but *not* the Brothers Karamazov, in only one single command.
1. OK, enough high-minded literature.  Let's dive into file systems. There is an innocent file trapped someplace under `folders/ohnoanotherfolder`. Browse through the folders, find him, and copy him to the `folders` folder *without using a pathname*.  (Hint: dots)
1. Now, look in the `man` page for `ls` (reproduced here <https://linux.die.net/man/1/ls> and find the 'recursive' operator.  Use this to instead to find the file above
1. Will has misplaced a very important file called 'youfoundit.txt' inside the hellscape that is the `foldersplosion` folder.  Find it, without using `find` or `locate`.
	- This is a bit tricky, as you don't want to look for it manually.  But there's a way to take the output of one command and pipe it to another command for searching to make this simple.
    - Now find it using `find`, a tool which is very powerful, but very opaque in its syntax. The man page for this program is missing on datahub, but it's also available at <https://linux.die.net/man/1/find>
1. Will's CV could use a bit of padding.  Please change the author of 'The Red Wheelbarrow' in `literature/wcw_barrow.txt` to read 'Will Styler, 2022'.  Use `nano` (or your cli editor or choice) to edit this file, or if you're experienced with the command line, find a way to do it without an editor.
1. You'd better change the name of the file too.  Turn that poem into `ws_barrow.txt`
1. Oh no, the academic integrity people have caught wind of my scheme!  Quick, hide the evidence by moving that modified file into a new folder called `academic_misdeeds` inside `foldersplosion/folder_2974_bbq`.  Do this in less than three commands.
1. That's it, if Will's going to be a fugitive from the academic law, you're going to join him.  Commit some unix crimes by moving around the file system and running commands such that you run into three `Permission Denied` or similar 'you can't do that' messages.
1. You'll need an alibi.  Create a new, empty file in your home folder called `alibi.txt`.  That should keep the UCSD IT people from searching you out.
1. First, **DO NOT RUN THE FOLLOWING COMMAND ON YOUR COMPUTER**. Oftentimes on the internet, trolls will attempt to convince people to run this **VERY DANGEROUS** command: `rm -rf /`, or occasionally, `rm -rf ~`. Think about the command, using the `man` page for `rm` if you need to, and then explain to your TA or instructor why it's a bad idea.  Feel free to run it ON DATAHUB.  They have protections in place, sadly.
1. Now, let's play Unix golf.  Try and do the following things in as few commands (e.g. enter presses) as possible:
	- Count the number of words in all the documents in the literature folder and save only the number of words to a file called `thatsalotofwords.txt`
	- Save a listing of all the files and folders, hidden or not, in `foldersplosion`, to a file called `whywillwhy.txt`
	- Change the name of `foldersplosion` to `abandonallhopeyewhoenterhere` *without leaving your home folder*
1. Come to think of it, foldersplosion is a liability by any name.  Delete that folder.
1. Finally, you're going to learn the most important skill for using the `vim` text editor: How to exit it if you end up there accidentally. We'll talk more about vim later, as it's incredibly powerful, but for now, open your previously created `alibi.txt` using vim with `vim ~/alibi.txt`.  Once you're there, type :q! to leave vim.
