# Install Git on Mac OS X
There are several ways to install Git on a Mac. In fact, if you've installed XCode (or it's Command Line Tools), Git may already be installed. To find out, open a terminal and enter `git --version`.

Apple actually maintain and ship [their own fork of Git](https://opensource.apple.com/source/Git/), but it tends to lag behind mainstream Git by several major versions. You may want to install a newer version of Git using one of the methods below:

### Git for Mac Installer
The easiest way to install Git on a Mac is via the stand-alone installer:

1. Download the latest [Git for Mac installer](https://sourceforge.net/projects/git-osx-installer/files/)
2. Follow the prompts to install Git.
3. Open a terminal and verify the installation was successful by typing `git --version`
4. Configure your Git username and email using the following commands, replacing the shown name with your own.
```
git config --global user.name "Peter Leonard"
git config --global user.email "peter@leonard.com"
```
### Install the git-credential-osxkeychain helper
Bitbucket supports pushing and pulling your Git repositories over both SSH and HTTPS. To work with a private repository over HTTPS, you must supply a username and password each time you push or pull. The git-credential-osxkeychain helper allows you to cache your username and password in the OSX keychain, so you don't have to retype it each time.

1. Open a terminal window and check: `git credential-osxkeychain`. If you receive a usage statement, skip to step 4. If the helper is not installed, go to step 2.
2. Use curl to download git-credential-osxkeychain (or [download it via your browser](http://github-media-downloads.s3.amazonaws.com/osx/git-credential-osxkeychain)) and move it to /usr/local/bin:
```
curl -O http://github-media-downloads.s3.amazonaws.com/osx/git-credential-osxkeychain
sudo mv git-credential-osxkeychain /usr/local/bin/
```
3. Make the file an executable: `chmod u+x /usr/local/bin/git-credential-osxkeychain`
4. Configure git to use the osxkeychain credential helper. `git config --global credential.helper osxkeychain`

The next time Git prompts you for a username and password, it will cache them in your keychain for future use.

# Install Git on Windows

1. Download the latest [Git for Windows installer](https://git-for-windows.github.io/).
2. When you've successfully started the installer, you should see the Git Setup wizard screen. Follow the Next and Finish prompts to complete the installation. The default options are pretty sensible for most users.
3. Open a Command Prompt (or Git Bash if during installation you elected not to use Git from the Windows Command Prompt).
4. Configure your Git username and email using the following commands, replacing the shown name with your own.
```
git config --global user.name "Peter Leonard"
git config --global user.email "peter@leonard.com"
```

# Install Git on Linux
## Debian / Ubuntu (apt-get)

1. From your shell, install Git using apt-get: `sudo apt-get install git-all`
2. Verify the installation was successful by typing `git --version`
3. Configure your Git username and email using the following commands, replacing the shown name with your own.
```
git config --global user.name "Peter Leonard"
git config --global user.email "peter@leonard.com"
```

## Fedora (dnf/yum)

1. From your shell, install Git using dnf (or yum, on older versions of Fedora): s`udo dnf install git` or `sudo yum install git`
2. Verify the installation was successful by typing `git --version`
3. Configure your Git username and email using the following commands, replacing the shown name with your own.
```
git config --global user.name "Peter Leonard"
git config --global user.email "peter@leonard.com"
```
