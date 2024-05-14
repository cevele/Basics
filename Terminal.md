# Terminal

## Overview:

This Markdown report is all about using the various functionalities of the terminal (in this case, the Mac and VSCode terminals).

The terminal is a fundamental tool for programming that makes you more efficient. The more and more comfortably you use it, the better a programmer you'll be.

Sections include:

1. General
2. Git
3. VSCode

## General:

### Contents of a Directory (Folder):

This is likely the most fundamental command. This helps you navigate and see which files are available to you. To do so, run the below command.

```
    ls -la
```

This will show you both visible and hidden files in a directory.

### Changing Directories (Folders):

To do this, you simply need to run the following command.

```
    cd <folder_name>
```

The above only works going forwards. If you want to go backwards, use the following:

```
    cd ..
```

If you want to go to the home directory:

```
    cd ~
```

If you want to the to go to the previous directory:

```
    cd -
```

### See Current Directory:

If you want to see which directory you are in (and get the full path), use the following

```
    pwd
```

## Git & Github:

### General:

For reference, all Git commands must start with the below:

```
    git
```

### Cloning an Existing Repository (Project):

This will allow you to download a repository from your VSCode to your local machine. This will copy all the files and folders, as well as the relevant Git version control files.

To do so, run the below command:

```
    git clone <SSH_key>
```

The SSH key can be found here in any repository:

![alt text] (SSH_Key.png)
<img src="SSH_key.png" alt="alt text">

A key thing here is that you'll know you're in a Git repository folder if there is a hidden _.git_ file

### Status of Files in Repository:

This is how you keep track of which files have had any changes, which files Git is tracking changes for and which files have yet to have their changes committed.

To do so, run the below command:

```
    git status
```

### Begin Tracking Changes:

This allow you to enable the Git version control functionalities. There are two ways to use it.

The below will ensure that all files in the relevant directory are tracked:

```
    git add .
```

The below will ensure that only a specified file in the relevant directory is tracker:

```
    git add <file_name>
```

### Commit Changes:

This is effectively Git's save functionality. It allows you to save all the changes you've made to the local _.git_ file.

This can be done using the following:

```
git commit -m <title_of_changes> -m <description of changes>
```

The important thing to remember here is that even though you've saved your changes, you've only done it on your local machine. This means that you're "golden source" (GitHub) has not been updated yet.

### Send Changes to GitHub:

This allows you to take all your tracked changes that you have committed and sync them to your GitHub profile.

This can be done with the following command:

```
    git push
```

You will be asked for your password.

## VSCode:

### General:

For reference, all VSCode commands must start with the below:

```
    code
```

### Creating and opening files:

```
    code <file_name>
```

### Opening Folders:

## SSH Keys:

### Overview:

SSH keys are a more secure way to download and send things via the internet.

Having different SSH Keys allows you to control who is able to access which things on your local machine and how.

### Generating a New SSH Key:

To generate a new key, you need to run this locally.

```
    ssh-keygen -t rsa -b 4096 -C <email_address>
```

The arguments here mean:

- -t = Type of Encryption
- -b = Strength of Encryption
- -C = Email Address

The email address should be the same as your GitHub email.

SSH keys are all saved in a default _/Users/cevele/.ssh/id_rsa_ folder.

You will get 2 prompts when running this:

1. Name your key (which is important if you have multiple)
2. Assign a password (increases security)

There are 2 keys that are created when you run this:

1. Public - this is the key that the external device that wants to access your local machine uses, and is fine to share (i.e.: upload to GitHub)
2. Private - this is the key that your local machine uses and must be kept secure.

The way it works is that the private key generates the public key. The private key is created in such a way that only the private key could possibly generate the public, thus authenticating that you are actually the person who granted this access.

### Checking for Existing SSH Keys:

You'll have to navigate to the SSH directory, which is the following:

_/Users/cevele/.ssh_

To see your keys, use:

```
    cat <key_name>
```

If you want to copy this key, use:

```
    pbcopy < file_path
```
