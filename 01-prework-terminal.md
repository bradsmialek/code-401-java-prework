# Prework - The Command Line

## Tasks
Working with Java and Android in this course will often involve interacting
with the terminal on our computers.

The assignment in this Pre-work will introduce you to some of the more common
commands involved in traversing directories and manipulating files on your
computer.

## Submitting Your Work
There will be an associated Canvas assignment available for you to submit
your completed work. For each of the following segments of
[Bash Command Line Tutorials](https://ryanstutorials.net/linuxtutorial/)
on ryanstutorials.net, you will completely read through and complete each of
the activities in your own terminal. As you complete each segment's
activities, take a moment to document your learnings and observations.

<ol>
  <li><a href="https://ryanstutorials.net/linuxtutorial/commandline.php">The Command Line</a> - What is it, how does it work and how do I get to one.</li>
  <li><a href="https://ryanstutorials.net/linuxtutorial/navigation.php">Basic Navigation</a> - An introduction to the Linux directory system and how to get around it.</li>
  <li><a href="https://ryanstutorials.net/linuxtutorial/aboutfiles.php">More About Files</a> - Find out some interesting characteristics of files and directories in a Linux environment.</li>
  <li><a href="https://ryanstutorials.net/linuxtutorial/manual.php">Manual Pages</a> - Learn how to make the most of the Linux commands you are learning.</li>
  <li><a href="https://ryanstutorials.net/linuxtutorial/filemanipulation.php">File Manipulation</a> - How to make, remove, rename, copy and move files and directories.</li>
  <li><a href="https://ryanstutorials.net/linuxtutorial/vi.php">Vi Text Editor</a> - Discover a powerful Linux based text editor.</li>
  <li><a href="https://ryanstutorials.net/linuxtutorial/wildcards.php">Wildcards</a> - Also referred to as globbing, this is a means to refer to several files in one go.</li>
  <li><a href="https://ryanstutorials.net/linuxtutorial/permissions.php">Permissions</a> - Learn to identify and change the permissions of files and directories and what the consequences of these are.</li>
  <li><a href="https://ryanstutorials.net/linuxtutorial/filters.php">Filters</a> - An introduction to various commands that allow us to mangle data in interesting and useful ways.</li>
  <li><a href="https://ryanstutorials.net/linuxtutorial/grep.php">Grep and Regular Expressions</a> - Master a powerful pattern matching language that is useful for analysing and processing data.</li>
  <li><a href="https://ryanstutorials.net/linuxtutorial/piping.php">Piping and Redirection</a> - Join commands together in powerful combinations.</li>
  <li><a href="https://ryanstutorials.net/linuxtutorial/processes.php">Process Management</a> - See what is currently running on your Linux system and what state the system is in, learn how to kill programs that have hung and put jobs in the background.</li>
  <li><a href="https://ryanstutorials.net/linuxtutorial/scripting.php">Scripting</a> - Be happy.  Get the computer to do tedious and repetitive tasks for you.</li>
  <li><a href="https://ryanstutorials.net/linuxtutorial/cheatsheet.php">Cheat Sheet</a> - A quick reference for the main points covered in this tutorial.</li>
</ol>

To submit your work in Canvas, copy the above list and paste each of your
meaningful observations and learnings below each section as a way to
illustrate and highlight things like 'ah hah' moments or really interesting
code snippets.

**Please note:** If you submit one-liners (i.e. "The permissions section
talked about permissions. It was cool.")_ you will not receive credit for
this assignment.

## Configure Your Bash Profile
Bash has a **Bash Profile** which is a file that allows you to configure
how your terminal behaves and define your own custom functions. Here's
some confiurations that set your default text editor and make it easy
for you to edit your profile in the future.

1. Run the command `touch ~/.bashrc ~/.bash_profile` to create these files.
2. Open the `~/.bash_profile` file in your text editor
3. To ensure `.bashrc` loads when the profile loads, add the following lines to
   the end of your `~/.bash_profile`
4. Add the additional functions to make it easy for you to edit your bash
   profile in the future.
5. Run `source ~/.bashrc` to load the new configuration.
6. Run `helpp` to execute your new, custom help command.

``` bash
# Read $HOME/.bashrc, if present.
if [ -f $HOME/.bashrc ]; then
  source $HOME/.bashrc   
fi
 
# set the default editor to VSCode
export EDITOR=code

# use "be" to edit your bash profile with the default editor
function be() {
  $EDITOR ~/.bash_profile
}

# use "br" this to refresh your bash profile after making any changes
function br() {
  source ~/.bash_profile
}

# create a shorthand "pingg" to ping google.com to see if you have a good
# internet connection.
function pingg() {
  ping google.com
}

# prints out all the custom commands we added to help remind you what exists.
# echo out more things yourself to remind you of other customizations you add!
# (there's two p's here because "help" is another built in command)
function helpp() {
  echo "be - edit your ~/.bash_profile"
  echo "br - refresh your ~/.bash_profile"
  echo "pingg - ping google.com (quit with CTRL+C)"
  echo "helpp - display this handy help reminder"
}
```
