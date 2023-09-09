# This is my outline for the nine topics covered, which includes 24 lessons 

### So first, I will write and describe all the bash and cmd commands I learned in this [course](https://practicum.yandex.ru/profile/git-basics/ "Git basics from Yandex") 

- **pwd** - print working directory

- **cd** - change directory

- **cd** ~ - change to the home directory

- **cd** .. - return to the parent directory

- **cd** / - go to the root directory

- **.** - access to the current directory

- **ls** - list directory contents

- **ls** -a - list directory all contents (-a = --all)

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

- You can use one **Tab** press for the autocomplete command or two **Tab** presses to display folders/files in the console

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