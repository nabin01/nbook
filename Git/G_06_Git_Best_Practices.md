# Git: Best practices

A git commit is like a checkpoint in your project. After you make a series of definitive changes, you commit them. However this raises several questions like:

- What files should I commit?
- Should I add every file to a commit? What about log files and binaries?
- How often should I commit?
- Should I commit every small change?

Find out good practices to git commit in this tutorial.

## Before we start

Remember that these are just guidelines that are supposed to make your work flow easier to manage. Following these will help you manage your projects later with much lesser hassle. However, feel free to try anything you want as you are developing your project. Especially when you are learning, it's important to try out different things so you know exactly what you are doing.

## What to commit

A project includes many files (build files, log files, large datasets and so on). However, not all of these files are of interest to version control. You don't need build files and log files to maintain the codebase. For example, you don't need the binaries since binaries keep changing with each change. Hence, you are better to exclude such files in your git commit.

Another important point to remember is to not commit a big file. Although git allows you to upload files as big as 100 MB (warns you for files greater than 50 MB and blocks files greater than 100 MB), it is not a good idea to commit big files. This, in a long run, will bloat your repository (even big image files will do this) and you don't want this, especially in a commercial environment.

If you are working with large files (like datasets for machine learning projects), host them on cloud (for instance: use google drive). If you are looking to host files for a smaller group of people (in your company or just a small collaborative project), look at git alternatives to share those files.

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
