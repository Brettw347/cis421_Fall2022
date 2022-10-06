# CIS 421: Project 1

## Created By:
Brett Williams

# Solution Log

## General Skills
---
### Challenge 1: Obedient Cat
### Point Value: 5 Points
### Objective: Read a file using the 'cat' command
#### Steps taken:
- Used the 'wget' command to download the file
- Used the 'cat' command on the 'flag' file
- Obtained the flag and completed the challenge
---

### Challenge 2: Tab, Tab, Attack
### Point Value: 20 Points
### Objective: Unzip the given file and find the flag
#### Steps taken:
- Used wget to download the file
- Used cat to read the file, nothing useful was found
- Used the 'less' command, found there are 8 files in the .zip folder
- Used unzip on the downloaded file
- Used the 'cd' command to enter the unzipped file
- Used 'cd' and hit tab to autocomplete the file path
- Used less and cat to try reading the file in the last directory, didn't find the flag
- Used the 'grep' command (grep -a picoCTF fang-of-haynekhtnamet) to find 'picoCTF' in the file, found the flag
---

### Challenge 3: Static ain't always noise
### Point Value: 20 Points
### Objective: Find the flag inside the file using the given bash command file
#### Steps Taken:
- Downloaded the given files using wget
- Used 'sh ltdis.sh static'to run the bash script on the file
- The script created the file, 'static.ltdis.strings.txt'
- Used 'cat static.ltdis.strings.txt' to see the text
- Used 'grep picoCTF static.ltdis.strings.txt' to find the flag
---

### Challenge 4: Nice netcat...
### Point Value: 15 Points
### Objective: Find the flag using
#### Steps Taken:
- Ran the given nc command but found nothing useful
- Ran the command again with '> flag' at the end to put the text in another file
- Use this website (https://www.duplichecker.com/ascii-to-text.php) to convert the ASCII numbers into text and found the flag
---

### Challenge 5: Magikarp Ground Mission
### Point Value: 30 Points
### Objective: Find the flag across multiple files in the given serve
#### Steps Taken:
- Connected to the serve via the given 'ssh' command
- Used ls to find the first part of the flag in a .txt file
- Used cat on the file and on the next .txt file
- Used 'cd /' to enter into another directory
- Found a .txt file containing another part of the flag
- Found another .txt file with instructions to get to the last part of the flag
- Used 'cd `' to get to the home file
- Found the last .txt containing the last part of the flag
---

### Challenge 6: Lets Warm Up
### Point Value: 50 Points
### Objective: Use the Linux command line to find the letter in ASCII of hexadecimal number 0x70
#### Steps Taken:
- Googled how to convert hexadecimal values to ASCII and found this website (https://www.baeldung.com/linux/character-hex-to-ascii)
- Used 'printf '\x70' to find the letter
- Submitted the answer in the picoCTF flag format (picoCTF{p})
---

### Challenge 7: Warmed Up
### Point Value: 50 Points
### Objective: Find the value of 0x3d in base 10 using the Linux Terminal
#### Steps Taken:
- Used 'printf '\x3D', which gave us the character '='
- Used 'man ascii' to open the manual for ascii and used the given chart to find the numeric value of '='
- Submitted the flag (picoCTF{61})
---

### Challenge 8: First Grep
### Point Value: 100 Points
### Objective: Find the flag by using the 'grep' command to look through a lenghty file
#### Steps Taken:
- Downloaded the given file with wget
- Used cat to view the file, found a lot of text but not the flag
- Used 'grep "picoCTF" file' to find the flag
---

### Challenge 9: fixme1.py
### Points Value: 100 Points
### Objective: Using the Linux terminal, download, fix, and run the given Python file
#### Steps Taken:
- Downloaded the given file
- Used 'nano fixme1.py' to edit the .py file
- Removed the indent in the print statement
- Successfully ran the python file, giving me the flag
---

### Challenge 10: Based
### Point Value: 200 Points
### Objective: Connect to a server by translating a password from binary into text
#### Steps Taken:
- Established the connection using the given command
- Recieved the binary numbers that need to be translated
- Tried using 'python hex()' and 'python int()' but kept getting errors
- Googled a binary to text converted (https://www.rapidtables.com/convert/number/binary-to-ascii.html)
- After entering the given password, I found out the server asks for more than one password
- I googled a solution since I couldn't figure out how to get the next password 
- I used this website which helped me find the solution (https://zomry1.github.io/based/)
- I had to convert three passwords from binary, octal, and hexadecimal before getting the flag
- Found the flag
---

## Web Explotation
### Challenge 1: Cookies
### Point Value: 40 Points
### Description: Find the Flag on the given website
#### Steps Taken:
- Opened the given website in a new tab
- The website prompted me to type in a certain kind of cookie
- Used the inspect tool on the home page
- Tried looking around through the inspect tool but couldn't find anything
- Tried submitting different types of cookies into the searchbar but didn't find anything
- Googled for a solution after not finding anything else (Website: https://dmfrsecurity.com/2021/08/23/picoctf-2021-cookies-writeup/)
- Went back to the inspect tool and went into the 'Application' tab and went to 'Cookies'
- At the home page, the value of 'name' was -1, but after typing in 'snickerdoodle' as the search bar prompts, it's value became 0
- Changed the value to 18 and refreshed the page
- Got the flag
---


### Challenge 2: Where are the robots
### Point Value: 100 Points
### Description: Find the robots.txt file on the website to find the flag
#### Steps Taken:
- Opened the given website in a new tab
- Added 'robots.txt' at the end of the url to take me to the sitemap
- Used the given url to get to the page where the flag was
---

## Cryptography
### Challenge 1: Mod 26
### Point Value: 10 Points
### Description: Find the flag by decypting the ROT13 code
#### Steps Taken:
- As the hint suggested, I used an online website to decode the flag for me (Website: https://rot13.com/)
- Copy and pasted the flag into the website and got the real flag
---

### Challenge 2: Easy1
### Point Value: 100 Points
### Description: Using the given key and encrypted flag, find the decrypted flag
#### Steps Taken:
- Clicked on the given table to download a .txt file
- Viewed the file and wrote out what I thought was the right flag
- Ended up being incorrect, looked online for solutions
- Found this website that explained it was a Vigenère cypher (Website:https://github.com/Dvd848/CTFs/blob/master/2019_picoCTF/Easy1.md)
- Used the given online decoder and found the flag
---

## Reverse Engineering
### Challenge 1: keygenme-py
### Point Value: 30 Points
### Description: Using the given program, find the code by figuring out how the program works and how to get the flag from it.
#### Steps Taken:
- Downloaded the given .py file into the shell
- Used the python command on the file to run it
- Tried the different menus the program prompts you to, couldn't find anything
- Exited the program and used cat on it to view the code
- Found part of the flag
- Found part of a password needed to be used in the program to unlock the 'full version'
- Found that the password has a part that is dynamically generated in the program
- Tried moving lines of code around and removing code but nothing worked
- Found a solution from this video (Video: https://www.youtube.com/watch?v=3dUXR3ftc50&ab_channel=AlmondForce)
- Using what was explained in the video, I was able to find the key
- The video explained the the dynamic part of the password is generated based on sha256 decryption used on the given username
- Combining parts of the decryption in a certain order with the static parts of the key gave me the flag
---

### Challenge 2: Safe Opener
### Point Value: 100 Points
### Description: Find the password to the 'safe' in the given java file to get the flag
#### Steps Taken:
- Downloaded the given java file to the shell
- Used the javac command to complie the file
- Used the java command to run the file
- Exited out of the prompt and used cat on the file to look at the code
- Found the password encrypted in Base64
- Copy and based the encrypted code into this website (Website: https://www.base64decode.org/)
- Used the password and it was correct. Submitted the password as the flag
---

## Forensics
### Challenge 1: information
### Point Value: 10 Points
### Description: Find the flag in the data of the given .jpg file
#### Steps Taken:
- Downloaded the file to the shell
- Used the cat command on the file but found nothing useful
- Used the nano command on the file and found some more information about the file
- I saw 'picoCTF' mentioned and clicked on the links that were displayed
- The one link was about metadata, so I'm assuming the metadata is important to this challenge
- I wasn't sure what to do next or had ideas on what else I could do, so I googled the challenge
- I found the solution here (Website: https://github.com/vivian-dai/PicoCTF2021-Writeup/blob/main/Forensics/information/information.md)
- They noticed this string of text 'cGljb0NURnt0aGVfbTN0YWRhdGFfMXNfbW9kaWZpZWR9', which I also saw when I used nano
- They put it through a base64 decrypter to find the flag, and I did the same
---

### Challenge 2: Enhance!
### Point Value: 100 Points
### Description: Find the flag in the given file
#### Steps Taken:
- Downloaded the file using the wget command
- Used the cat command on the file but didn't find anything useful
- Opened the file through the nano command
- Clicked on the links displayed but didn't find anything useful
- Used the less command to see if it would display differently from the cat command
- I noticed in the last section of the file, sections of the flag were scattered in each line
- I combined the parts to get the flag
---

## Binary Exploitation
### Challenge 1: Cache Me Outside
### Point Value: 70 Points
### Description: Find the flag using heap allocations
#### Steps Taken:
- As the hint suggested, I looked up GLIBC's tcache to learn more about it (Website: https://azeria-labs.com/heap-exploitation-part-2-glibc-heap-free-bins/)
- It seems that the tcache used seems to speed up requests to a server, but causes the server to be more vulnerable to attacks
- Downloaded the given files with wget
- Tried connecting to the given server to see what is happening
- Server prompted to change a byte in the program and is asking for an Address
- Unsure of what to do, I used cat on each of the downloaded files, still wasn't sure what else I could do
- Tried using the strings command on each of the files but didn't find the flag
- Tried using the grep command but didn't find the flag
- I ended up searching online for a solution (Website: https://github.com/Dvd848/CTFs/blob/master/2021_picoCTF/Cache_Me_Outside.md)
- I still have a hard time understanding what is going on, but I think the program wants you to call a heap and have it point to another one to get the flag
---

### Challenge 2: Unsubscriptions Are Free
### Point Value: 100 Points
### Description: 
#### Steps Taken:
- Downloaded the given files onto the shell using wget
- Looked at the hint which led me to a pdf explaining heap overflow and double-free attacks
- After reading the pdf, went to the shell and connected to the provided server
- Saw the menu options and went through each of them
- While going through the menu options, I got a timeout
- I used cat, nano, and less on the downloaded files
- in the vuln.c file, I found a 'flag.txt' mentioned in a function, leading me to try and find a way to get to call that function.
- I went back to the server and connected, and noticed a 'memory leak' with a value in
- Tried to find a way to change the 'memory leak' into text but couldn't find anything
- Tried modifying the code of the program and compiling it with the 'gcc' command
- Ran the file but still didn't get the flag
- Wasn't sure what else to try, so looked up a solution (Website: https://www.youtube.com/watch?v=ffJRcNEyApI)
- He explains in the video that memory needs to be freed than reallocated so that it can be accessed
---

## Highest Difficulty
### Challenge Name: Java Script Kiddie 2
### Point Value: 500 Points
### Description: Fix the given link using Java Script and find the flag
#### Steps Taken:
- Went into the shell and tried to connect in the shell using the nc command, but was told I was missing the port number
- Copy and pasted the link into Google and was brought to a website prompting me to enter something into a search box
- Looked at the page source, found nothing useful
- Used the inspect tool
- Found a variable called 'key', tried to copy and paste it into the search box, it didn't work
- Continued looking around with the inspect tool, but couldn't find anything
- Wasn't sure what else to do, looked for a solution online (Website: https://blog.srikavin.me/posts/picoctf-2019-java-script-kiddie-2/)
- The challenge is similar to a previous one, which I didn't do, so it was hard for me to understand it all
- From what I gathered, it seems that a script was created from the last challenged and slightly modified to get a code
- This code then had to be converted from base64 and inserted into the given website's search bar, revealing a QR code that contains the flag
---
