Before Dracula can connect to a remote repository, he needs to set up a way for his computer to authenticate with GitHub so it knows it’s him trying to connect to his remote repository.

We are going to set up the method that is commonly used by many different services to authenticate access on the command line. This method is called Secure Shell Protocol (SSH). SSH is a cryptographic network protocol that allows secure communication between computers using an otherwise insecure network.

SSH uses what is called a key pair. This is two keys that work together to validate access. One key is publicly known and called the public key, and the other key called the private key is kept private. Very descriptive names.

You can think of the public key as a padlock, and only you have the key (the private key) to open it. You use the public key where you want a secure method of communication, such as your GitHub account. You give this padlock, or public key, to GitHub and say “lock the communications to my account with this so that only computers that have my private key can unlock communications and send git commands as my GitHub account.”

What we will do now is the minimum required to set up the SSH keys and add the public key to a GitHub account.

<br/>

The first thing we are going to do is check if this has already been done on the computer you’re on. Because generally speaking, this setup only needs to happen once and then you can forget about it.

We will run the list command to check what key pairs already exist on your computer.
> `ls -al ~/.ssh`{{execute}}

If SSH has been set up on the computer you’re using, the public and private key pairs will be listed. The file names are either id_ed25519/id_ed25519.pub or id_rsa/id_rsa.pub depending on how the key pairs were set up.

If SSH does not exist on your computer, you can create them by the following bash:
> `ssh-keygen -t ed25519 -C "your_email@example.com"`{{copy}}
> `ssh-keygen -t rsa -b 4096 -C "your_email@example.com"`{{copy}}

It will show the output:
> ```
> Generating public/private ed25519 key pair.
> Enter file in which to save the key (/c/Users/Vlad Dracula/.ssh/id_ed25519):
> ``` 

We want to use the default file, so just press <kbd> Enter </kbd>, and show the following output:
> ```
> Created directory '/c/Users/Vlad Dracula/.ssh'.
> Enter passphrase (empty for no passphrase):
> ```

Now, it is prompting user for a passphrase to raise security. Be sure to use something memorable or save your passphrase somewhere, as there is no “reset my password” option.

`Enter same passphrase again:`

After entering the same passphrase a second time, we receive the confirmation
> ```
> Your identification has been saved in /c/Users/Vlad Dracula/.ssh/id_ed25519
> Your public key has been saved in /c/Users/Vlad Dracula/.ssh/id_ed25519.pub
> The key fingerprint is:
> SHA256:SMSPIStNyA00KPxuYu94KpZgRAYjgt9g4BA4kFy3g1o vlad@tran.sylvan.ia
> The key's randomart image is:
> +--[ED25519 256]--+
> |^B== o.          |
> |%*=.*.+          |
> |+=.E =.+         |
> | .=.+.o..        |
> |....  . S        |
> |.+ o             |
> |+ =              |
> |.o.o             |
> |oo+.             |
> +----[SHA256]-----+
> ```

The “identification” is actually the private key. You should never share it. The public key is appropriately named. The “key fingerprint” is a shorter version of a public key.

Now that we have generated the SSH keys, we will find the SSH files when we check.
> `ls -al ~/.ssh`{{execute}}

Now we run the command to check if GitHub can read our authentication. First, we need to copy the public key. Be sure to include the `.pub` at the end, otherwise you’re looking at the private key.
> `cat ~/.ssh/id_ed25519.pub`{{execute}}

Now, going to GitHub.com, click on your profile icon in the top right corner to get the drop-down menu. Click “Settings,” then on the settings page, click “SSH and GPG keys,” on the left side “Account settings” menu. Click the “New SSH key” button on the right side. Now, you can add the title (Dracula uses the title “Vlad’s Lab Laptop” so he can remember where the original key pair files are located), paste your SSH key into the field, and click the “Add SSH key” to complete the setup.

Now that we’ve set that up, let’s check our authentication again from the command line.
> `ssh -T git@github.com`{{execute}}

You are being authenticated in GitHub.

<br/>















