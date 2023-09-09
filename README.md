# This is my outline for the nine topics covered, which includes 24 lessons 

### So first, I will write and describe all the bash and cmd commands I learned in this [course](https://practicum.yandex.ru/profile/git-basics/ "Git basics from Yandex") 

- **pwd** - print working directory

- **cd** - change directory

- **cd** ~ - change to the home directory

- **cd** .. - return to the parent directory

- **cd** / - go to the root directory

- **.** - access to the current directory

- **ls** - list directory contents

- **ls** **-a** - list directory all contents (-a = --all)

- **touch** - create new file

- **mkdir** - make new directory

- **mkdir** **-p** - create directory structure

- **cp** - copy file or directory

- **mv** - move files or directory

- **cat** - read file. works only with text files *from eng. concatenate and print*

- **rm** - remove file

- **rmdir** - remove directory

- **rm** **-v** - remove recursive. *use carefully removes at once*

----
**All delete commands erase data irretrievably - it cannot be recovered from the Recycle Bin!**
----

### Helpful features

- You can use two ampersands to use two commands at once at the same time (**&&**).

- You can use past commands by using **↑** or **↓**

- You can use **one Tab** press for the autocomplete command or **two Tab** presses to display folders/files in the console

### Git setup
1. [download git](https://git-scm.com/downloads)

2. configuration setup
``` bash
git config -g user.name "your name"
git config -g user.email your@email.git
#-g = --global
```

3. check the configuration
``` bash
#use the first or second command
cat ~/.gitconfig 
git config -l
# -l = --list
```

## Using git

-  Initialize git 
``` bash
cd ~/dev/firstProject # go to the desired folder
git init # git initialization
```

- To delete a git repository if you mess up the folder. I mean, delete the git folder.
``` bash
cd <repository folder>
rm -rf .git
# r = recursive, f = force
```

- **Git status** - it shows the current state of the repository.

- Preparing a file for saving
``` bash
git add file.txt
```

to add the whole folder
``` bash
git add .
```

- How to make commit
``` bash
git commit -m "First commit"
# m = message
```

- How to check commit history
``` bash
git log
```

## Generating SSH-key

1.
``` bash
ssh-keygen -t ed25519 -C "email to which your GitHub account is linked"
# But if u have error, use next command
ssh-keygen -t rsa -b 4096 -C "email to which your GitHub account is linked"
```

2. Press **Enter**

3. The programm will ask for a passphrase to access the SSH-key. You can leave th e field blank. To do so, press Enter and the press Enter again to confrim.

4. Done! Now it remains to verify that the keys have indeed been generated. To do so, call this command.
``` bash
ls -a ~/.ssh
```

### Linking to GitHub

1. copy your key
``` bash
# for windows

clip < ~/.ssh/id_rsa.pub
# for ed25519:
clip < ~/.ssh/id_ed25519.pub
```

2. Go to **Settings** in GitHub.

3. Go to point **SSH and GPG keys**.

4. Press button **New SSH key**.

5. Fill **Title**. For example: Personal key.

6. **Key Type** -> **Authentication Key**.

7. Paste your key in field **Key**.

8. Press button **Add SSH key**.

9. Verify that the key is correct using the following command.
``` bash 
ssh -T git@github.com
```

If it's first time, when u use Git, to share a project on GitHub a similar warning will appear.
``` bash
The authenticity of host 'github.com (140.82.121.4)' can't be established. ED25519 key fingerprint is SHA256:+DiY3wvvV6TuJJhbpZisF/zLDA0zPMSvHdkr4UvCOqU. This key is not known by any other names. Are you sure you want to continue connecting (yes/no/[fingerprint])?
```

write **yes**

``` bash
Hi %Your_Account%! You've successfully authenticated, but GitHub does not provide shell access.
```

### Linking local and remote repositories

- Go to the remote repository page, select SSH type and copy the URL. 

- Open bash and navigate to the local repository directory and enter the command
``` bash
cd ~/dev/firstProject
git remote add origin https://github.com/revlze/PracticalWork-1 # use ur link
```

- Make sure the repositories are linked.
```bash
git remote -v
# -v = verbose
```

### Send the change to a remote repository

``` bash
git add file.txt
git commit -m "added file.txt"

git push -u origin master

#if u got error use other command

git push -u origin main
```

**git push -u origin master** - this command is needed only for the first time, for the next time you need to use this command - **git push**

### About Markdown

cheet sheet - https://gist.github.com/fomvasss/8dd8cd7f88c67a4e3727f9d39224a84c


*end.*