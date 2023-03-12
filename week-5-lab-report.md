# Week 5 Lab Report

For this week's lab report, I will essentially "redo" lab report 3 with an exploration of options for a different command: `less` (as opposed to `grep`).
Like last time, I will provide 4 options with around 2 examples each of the options in use. 


Option #1: `-E`
---

The `-E` command makes `less` automatically exit after coming to the end of the file. 

Examples on ./written_2:

1.
![Image1](https://user-images.githubusercontent.com/122575873/224565638-2d18442e-ea3a-4744-b706-fa61740d65d8.png)
![Image2](https://user-images.githubusercontent.com/122575873/224565685-7ea20d71-ae20-45ee-a4d4-02b443298d0f.png)
![Image3](https://user-images.githubusercontent.com/122575873/224565705-185c0731-cb49-428d-bce3-42acb7f6eee5.png)

2.
![Image4](https://user-images.githubusercontent.com/122575873/224565910-524e8859-8d6d-477c-86b7-c45c795d4144.png)
![Image5](https://user-images.githubusercontent.com/122575873/224565963-8a83568e-e0cf-4c72-ad8d-e110a14a53e7.png)
![Image6](https://user-images.githubusercontent.com/122575873/224566013-9d0d2585-5a45-41c3-b2e9-88627815ad53.png)


It's hard to properly see with only screenshots, but after I scroll down to the bottom of the file it automatically exits back to the command line.
This command option is particularly useful if you're in a hurry or forgot the keystroke to exit out of a file (`q`). 


Option #2: `-I`
---

Similar to grep, the `-I` command for `less` makes the search case-insensitive. 

Examples on ./written_2:
1. ![Image7](https://user-images.githubusercontent.com/122575873/224566942-39edca0c-bee3-4043-9c19-521143db180a.png)
![Image8](https://user-images.githubusercontent.com/122575873/224566959-298183b7-bb3a-42ef-96ea-395303e97472.png)

2. ![Image9](https://user-images.githubusercontent.com/122575873/224566987-6b437920-18c3-4cfb-97f7-27889abd4971.png)
![Image10](https://user-images.githubusercontent.com/122575873/224567004-774d298b-f22b-4240-8471-97be1bc5555d.png)


You can press `/` and then type your search term to search the file with `less`. The found words/phrases are highlighted.
Normally, `less` is case-sensitive, but using the `-I` option renders it case-insensitive (including capital letters).
Here, I search for "economics" as well as "eCoNoMicS" and "EconoMiCs" in `ch15.txt`. They all return the same results, as expected. 

Note that while I was just checking the first returned result for these search terms, you can move to the next instance found by pressing `n` or go back by pressing `N`.
`less -i` is just like find and replace sans the replace. 


Option #3: `-g`
---

The `-g` command highlights the last searched-for String. (By default, `less -g` highlights every String matching the last search command.)

Examples on ./written_2:
1. ![Image13](https://user-images.githubusercontent.com/122575873/224567442-e5b4afdc-e323-4d58-ade4-50b5ebee2c33.png)
![Image11](https://user-images.githubusercontent.com/122575873/224567387-262f6a2a-01f8-40fd-9ba4-17cc96dfec34.png)

2. ![Image12](https://user-images.githubusercontent.com/122575873/224567410-0165015e-39f1-4c62-a2aa-7473ea8167a4.png)


This command is mostly self-explanatory.
As you can see in the examples above, the searched-for String is highlighted after I press enter on the search command.
It's not especially useful since you probably won't forget what you just searched for. 

Option #4: `-J`
---

The `-J` command pulls up a status column that shows the lines matching the current search term.
(It also shows lines marked using the `-m` or `-M` options, which are similar to the `more` command in that they're like `less` with *less* functionalities). 

Examples on ./written_2:
1. ![Image16](https://user-images.githubusercontent.com/122575873/224568187-b6886ad2-f87c-4072-8f62-b107e3cc892a.png)
![Image14](https://user-images.githubusercontent.com/122575873/224568209-d3d5cba1-0c54-4691-8436-2004793e06ba.png)

2. ![Image15](https://user-images.githubusercontent.com/122575873/224568120-cd8d88f5-c7b3-4c55-960a-c09d3532dfef.png)


After I use the `-J` command, a status column shows up in the lefthand side of the screen, marking lines that contain the search term with an asterisk. 
This might help if you want to visually gauge how prevalent your search term is in the file. 


Sources:

[Less Command in Linux](https://phoenixnap.com/kb/less-command-in-linux)

[Use Less, More, and Most Linux Commands](https://www.makeuseof.com/use-less-more-and-most-linux-commands/#:~:text=What%20Is%20the%20less%20Command,to%20load%20the%20whole%20file.)

[How to Use the Less Command on Linux](https://www.howtogeek.com/444233/how-to-use-the-less-command-on-linux/)
