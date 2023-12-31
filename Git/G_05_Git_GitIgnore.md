# Git: gitignore

You don't need all of the files in your project root folder. There are log files, back up files used by your text editor and other tools. There are binary files, very large files such as databases and more that only bloat up your repository and don't have any value to your actual source code or the running of your project because they are generated by other tools as required for every machine. Use gitignore to tell git to ignore these files from version control.

## gitignore: Don't track these files

- log files (.log)
- Back up files
- Files generated from other source files (eg. make files, if you use make or rake)
- Binary files
- Large files (datasets)
- .gitignore

Add all the files you don't want to track in .gitignore file. You can create a .gitignore file while creating repository in github by choosing the gitignore of your language or by manually creating .gitignore and adding a list of files for git to ignore.

There are various ways of configuring .gitignore. You can have a global .gitignore file that applies to all git projects in your machine. You can also have a local .gitignore file for each directory (git repository). Use a local .gitignore file for more control.

The following is an example of gitignore for a C/C++ project. Note that this is just an example and you will need to configure it as required by your project hierarchy. You can add other items (thumbs.db or desktop.ini files in windows and .Trash files in Linux). This is minimal but the principle here is important. All of the rules work recursively as well.

```
# backup and swap files for emacs and vim respectively
*~
*.swp

# setup your build to take place in a sub-directory called 'build'
# ignore that sub-directory
build/

# alternatively exclude all files with their extensions

# make files
*.lst
*.o
*.eep
*.lss
*.map
*.sym

# other generated files: object files, libraries, dlls and executables
*.obj
*.lib
*.so
*.dll
*.exe
*.out

# data folder - not required for smaller datasets
data/
```

If you mostly work with a fixed set of tools (your favourite IDE and a specific language), consider making a global ~/.gitignore_global file. It works for all of your git projects but you will need to tell git explicitly about the global gitignore file.

An example for Linux OS is:

```
# backup files
*~
.*~
*.swp

# Add other rules for projects you do
# C
# Object files
*.o
*.ko
*.obj
*.elf

# Linker output
*.ilk
*.map
*.exp

# Libraries
*.lib
*.a
*.la
*.lo

# Executables
*.exe
*.out

# add more as you require
```

Tell git about this .gitignore_global file:

```
$ git config --global core.excludesfile ~/.gitignore_global
```

The above command will make every git repository in your machine use the global .gitignore_global file.

## How often to commit

Committing every minor changes make your project history difficult to read. This in turn makes your workflow complex.

Consider the following factors before making a git commit:

- What major task (fixing a bug, adding/removing a feature) are you working on?
- Is the task complete?
- Does this new change work? (Test your code after every change and make sure it works and it has not broken other parts of the project)

## A good commit message

Commit with an appropriate message (short, concise not more than 60 characters), like a subject for an email.  A good commit message answers the question '**what does this commit do?**' and not '**what did I do?**'.

A short and concise commit message makes it easier to understand commits when you read your commit history.

If you require to write a long description (details) for this commit, first write an initial commit message (like an email subject) that explains what this commit contains. Then, describe the changes in subsequent lines (like an email body).

Here are a few examples: If you fixed a bug, write 'Fix bug <bug_id>' in your commit message. If you added a feature, write 'Add send message feature on Products page' in your commit message.

## Conclusion

Remember three important things:

- Commit after every major or a definitive change (like a checkpoint in a video game).
- Write a short and precise commit message, one that explains the change it contains.
- Don't bloat your repository. Use gitignore wisely.

Don't worry about getting everything right when you are learning. Keep working on projects. As you move further, you will get the idea of what to do, what not to do and what best fits your purpose. The best way to do this is to use git in every project you build, even if you just commit and push changes. As you get familiar, you will see that commits, gitignore and other features of git make your work-flow efficient and easier to manage.
