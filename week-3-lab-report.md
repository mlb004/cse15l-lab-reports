# Week 3 Lab Report

For this week's lab report, I chose the `grep` command to research. I will provide 4 options with around 2 examples each of these options in use.


Option #1: `-i`
---

The `-i` command for grep renders the search case-insensitive. 

Examples on ./written_2:
1. ![Image](https://user-images.githubusercontent.com/122575873/218336365-8950092c-fcb0-4ffe-9228-4cb612262ea3.png)
2. ![Image2](https://user-images.githubusercontent.com/122575873/218336381-d87e36a9-0ab1-4930-8be0-9d762045ecca.png)
3. ![Image3](https://user-images.githubusercontent.com/122575873/218336395-e053aa10-159c-4df1-b487-33818c71dcdf.png)


As shown above, when I vary the number of capital letters in the String "Bahamas" with the `-i` option added on the command line, the returned files are the same.


Sources:

[Wikibooks](https://en.wikibooks.org/wiki/Grep)


Option #2: `-v`
---

The `-v` command searches for non-matching lines to the input String (thus "inverting" the search process).

Examples on ./written_2:
1. ![Image7](https://user-images.githubusercontent.com/122575873/218337551-6b640605-93c2-435d-8f67-93a8fc0113a3.png)
2. ![Image8](https://user-images.githubusercontent.com/122575873/218337890-a87e5503-4dd5-4bb0-8eb7-3937e03d1f9a.png)


Not all files are shown! There are quite a lot of them!

The search process is inverted with `-v` and all files that don't contain "History" (including ones with "history" in them, as this grep search is still case-sensitive) are returned. 
The same idea is applied to "Where" in the second example.

Sources:

[Wikibooks](https://en.wikibooks.org/wiki/Grep)

[LibreTexts](https://eng.libretexts.org/Bookshelves/Computer_Science/Operating_Systems/Linux_-_The_Penguin_Marches_On_(McClanahan)/05%3A_File_and_Directory_Management/4.07%3A_Handling_Text_Files/4.07.04%3A_Handling_Text_Files_-_grep_Command)

[Using Grep](https://www.pair.com/support/kb/paircloud-grep/)


Option #3: `-c`
---

The `-c` command counts the number of lines that match the input String (useful for when you just need to know the number of matching files). 


Examples on ./written_2:
1. ![Image4](https://user-images.githubusercontent.com/122575873/218336931-7afe3a19-80f3-4c6d-9478-21f2d6c9bf09.png)
2. ![Image5](https://user-images.githubusercontent.com/122575873/218337096-42643026-47b0-48f5-b139-3c97787af509.png)


All files in written_2 are listed even though they are not shown here.
As you can see, the `0` at the end of each line means that there are zero lines that contain the input String in each file.
For the file that does contain "Lucayans", that number is nonzero.


Sources:

[Wikibooks](https://en.wikibooks.org/wiki/Grep)

[Using Grep](https://www.pair.com/support/kb/paircloud-grep/)


Option #4: `-h`
---

The `-h` command returns files with matching lines without prefacing them with the file name. 

Examples on ./written_2:
1. ![Image10](https://user-images.githubusercontent.com/122575873/218338493-cef007cc-37b1-43db-b61d-29503fae6125.png)
2. ![Image11](https://user-images.githubusercontent.com/122575873/218338669-7518aba5-71c3-4033-9309-f28f5ef38043.png)


In the first example, the titles of the files within `grep-results.txt` including "What" are highlighted in red (`-h` ensures `grep-results.txt` is not returned, just the contents that contain "What"). 
In the second example, the instances of "Nepal" within `Nepal-WhatToDo.txt` are highlighted in red without the file name also being outputted.

Sources:

[Wikibooks](https://en.wikibooks.org/wiki/Grep)

[ChatGPT](https://chat.openai.com/chat)
