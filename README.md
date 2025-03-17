# Bandit1-10OneHourSpeedrunChallenge
My journey running through Bandit 1-10 with explained steps along with timestamp proofs on the upper center of each image. I ended up failing this challenge I admit but still wanted to showcase my journey

*12:34 P.M* booted into ssh and typed bandit0 as the bandit password
![IMG_1415](https://github.com/user-attachments/assets/db4fb8c4-576a-449f-a30c-adbae704cb27)

*12:35 P.M* Found the password for bandit2. I did this by List files in the directory using BASH ls and Use CAT on the readme file that appears 
![IMG_1416](https://github.com/user-attachments/assets/ac747f64-cbf4-455a-8f11-5122b0a2ccb9)

*12:41 P.M* Found the password for bandit3. I did this by Use BASH cd ~ Display contents of hyphenated file using cat -
![IMG_1418](https://github.com/user-attachments/assets/68bb468c-b2cc-4968-89be-dfca555ed375)

*12:48 P.M* Found password for bandit4. I typed cat spaces\ in\ this\ file\ name to reveal the password
![IMG_1420](https://github.com/user-attachments/assets/c9cb333e-0c03-4461-aaf8-b5089173b363)

*1:00 P.M* Admittly got stumped around this area but found password for bandit5. I took advantage of the find key and typed find . -type f -size 1033c ! -executable. Basically, it finds a non-executable file with a very specific size in the current directory so I can be able to find the password
![IMG_1425](https://github.com/user-attachments/assets/cd11ca1f-94dc-4a9c-a1a0-b43bf66b50bb)

*1:08 P.M* Admittly got slightly stumped here too but found password for bandit6. The password was being hidden in a bunch of files, so I used find / -user bandit7 -group bandit6 -size 33c 2>/dev/null. That means: search the whole system (/), find files owned by bandit7 and in the bandit6 group, exactly 33 bytes long, and ignore errors. The password was in the file that matched. Why? Because that's the specific file they set up for us to find with those exact properties.
![IMG_1427](https://github.com/user-attachments/assets/524bf4f4-a0b6-4d5b-b0de-3bca5b1be2f9)

*1:16 P.M* This one was all about filtering log files. They gave us a log file, and the password was hidden in a line with the word 'millionth'. So, I just used grep millionth data.txt. That searches 'data.txt' for any line containing 'millionth', and bam, there's the password. Why? Because that's the only line they put in there with the password, specifically marked by the word 'millionth'.
![IMG_1429](https://github.com/user-attachments/assets/c7efde00-3ff4-46b9-89f2-f34a9e4ada7a)

*1:26 P.M* Bandit 8, that one was tricky with the multiple password possibilities. They gave us a file, data.txt, sorted, but with duplicate passwords. So, I used sort -u data.txt. That command sorts the file and removes any duplicate lines, leaving only the unique password. Why? Because the level's goal was to extract the unique password from a list of duplicates, and sort -u does exactly that.
![IMG_1430](https://github.com/user-attachments/assets/f739e9ae-fb1c-4c9e-b036-0f3680f2cab4)

Overall I set my excpectations to high and failed but still wanted to provide content 
