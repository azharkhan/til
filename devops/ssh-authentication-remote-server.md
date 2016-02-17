# Adding SSH Authentication to a Remote Server

## Create a key pair and choose a passphrase

> This is optional if you already have an existing key pair that you would like to use.

    ssh-keygen

    Generating public/private rsa key pair.
    Enter file in which to save the key (/Users/azhar/.ssh/id_rsa):
	Enter passphrase (empty for no passphrase):
	Enter same passphrase again:
	Your identification has been saved in /Users/azhar/.ssh/id_rsa.
	Your public key has been saved in /Users/azhar/.ssh/id_rsa.pub.
	The key fingerprint is:
	12:af:87:ca:ff:68:76:df:12:df:34:00:22:4a:88:4c azhar@Macbook
	The key's randomart image is:
	+--[ RSA 2048]----+
	|        ..       |
	| K       ..      |
	|o .     .o       |
	|=o      +..      |
	|=o     oXo       |
	|o .     -        |
	|   . o = o       |
	|    . + +..      |
	|       =...      |
	+-----------------+

## Copy the key to your clipboard

You can use whichever method you like, I prefer the following on OSX:

`cat /Users/azhar/.ssh/id_rsa.pub > pbcopy`

## Login to the remote server

> You should have root level access on this server in order to do this

Use the text editor of your choice (I like VIM) and paste the copied key above into the `~/.ssh/authorized_keys` file

## Try logging in via SSH and you should not be prompted for a password!

For an optional step you can disable password authentication altogether.

Edit your /etc/ssh/sshd_config file and add these lines:

PasswordAuthentication no
ChallengeResponseAuthentication no


[Source](https://blog.0xbadc0de.be/archives/300)
