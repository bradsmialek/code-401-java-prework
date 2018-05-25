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

1. [The Command Line]()
1. [Basic Navigation]()
1. [More About Files]()
1. [Manual Pages]()
1. [File Manipulation]()
1. [Vi Text Editor]()
1. [Wildcards]()
1. [Permissions]()
1. [Filters]()
1. [Grep and Regular Expressions]()
1. [Piping and Redirection]()
1. [Process Management]()
1. [Scripting]()
1. [Cheat Sheet]()

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
