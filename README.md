# This is my outline for the nine topics covered, which includes 24 lessons 

### So first, I will write and describe all the bash and cmd commands I learned in this [course](https://practicum.yandex.ru/profile/git-basics/ "Git basics from Yandex") 

- **pwd** - print working directory

- **cd** - change directory

- **cd** ~ - change to the home directory

- **cd** .. - return to the parent directory

- **.** - access to the current directory

- **ls** - list directory contents

- **touch** - create new file

- **mkdir** - make new directory

- **mkdir** **-p** - create directory structure

- **cp** - copy file or directory

- **mv** - move files or directory

- **cat** - read file. works only with text files *from eng. concatenate and print*

- **rm** - remove file

- **rmdir** - remove directory

- **rm** **-v** - remove recursive. *use carefully removes at once*

---
**All delete commands erase data irretrievably - it cannot be recovered from the Recycle Bin!**
---

### Setup GIT
1. [download git](https://git-scm.com/downloads)

2. your configuration -g = --global
``` bash
git config -g user.name "your name"
git config -g user.email your@email.git
```

3. check your configuration -l = --list
``` bash
#use the first or second command
cat ~/.gitconfig 
git config -l
```



