# Wargames
The 0verTheWire wargames are games designed to help you practice security concepts.  
There are a lot of categories, each including different leves. The most basic category, intended for beginners, is Bandit. It is a good way to get started. This is a list of the intended order to play the games: 
1. Bandit
2. Natas
3. Leviathan
4. Krypton
5. Narnia
6. Behemot
7. Utumno
8. Maze
9. Vortex
10. Semtex
11. Manpage
12. Drifter

## Bandit
This first section is designed to explain the basics of commands, ssh, etc. 
### Level 0
This one is only designed to test if you are able to ssh to the lab. 

Used commands: 
```bash
ssh bandit0@bandit.labs.overthewire.org -p 2220
bandit0
```

### Level 1
In this one, we only need to access a folder named "-".  
Due to the file name being -, we cant just access it directly. So...
```bash
ssh bandit1@bandit.labs.overthewire.org -p 2220
cd ./-
```

### Level 2
In this level, it is the same, but we only really need to tab the name of the file
```bash
ssh bandit2@bandit.labs.overthewire.org -p 2220
cat "spaces in this filename"
```

### Level 3

In this level, the file we need is hidden, so we really only need to access it.
```bash
ssh bandit3@bandit.labs.overthewire.org -p 2220
cd inhere/
cat .hidden
```