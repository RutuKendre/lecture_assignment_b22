## Assignment and Lecture Repository for b22
1)level 0
for level zero I got hints from the helpful reading material provided there itself.So I logged in using the command ssh -p 2220 bandit0@bandit.labs.overthewire.org and entere the password given in the question.

2)level 1
password:boJ9jbbUNNfktd78OOpsqOltutMc3MY1
I want into the home directory using cd ~
Then I checked if the readme file exists there using ls
Searched for the commands given in the hints and read the file using cat readme and  got the password
 
3)level 2
password:CV1DtqXWVFXTvM2F0k09SHz0YwRINYA9
The only difference from the previous level was to read a file whose name was -
So I read the given in the hints for dashed filename and serched for the command to read such files

3)level 3
password:UmHadQclWmgdLOKQ3YNgjWxGoRMb5luK
Again got hints from the reading material provided there and used the command cat "spaces in this file" to read a file whose name contains spaces.

4)level 4
password:pIwrPrtPN36QITSp3EQaw936yaFoFgAB
In this level the file was hidden in inhere directory.A command to list hidden files was taught in the lecture so I found out the filename using (ls -a) and read the file.

5)level 5
password:koReBOKuIDDepwhWk7jZC0RTdopnAYKh
Here the password was stored in a human readable file. I manually checked all the files and only file07 containes human readable content. 


6)level 6:
password:DXjZPULLxYr17uwoI01bNLQbtFemEgo7
Here I searched for required file using command (find . -type f -size 1033c ! -executable -exec file {} + | grep ASCII).Password was there in the file .file02 in maybehere07 file.But there were two files with similar names and the required file was hidden.So I had to use ls -a command.


7)level 7:
password:HKBPTKQnIay4Fw76bEy8PVxKEDQRKTzs
I found the file meeting required conditions using (find / -user bandit7 -group bandit6 -size 33c) In that I found /var/lib/dpkg/info/bandit7.password
.By using cat on it I got password.

8)level 8:
password:cvX2JJa4CFALtqS87jk27qwqGhBM9plV
I used grep command to find a match in given file(grep -n "millionth" data.txt).I randomly searched for grep command as it was mentioned in hnts.

9)level 9
password:UsvVyFSfZZWbi6wgC7dAFyFuR6jQQUhR
Here I used the command which reads data from file data.txt and then sorts it and finds the line that occurs only once.The command used is (cat data.txt | sort | uniq -u).
Here we have to sort forst because uniq deletes only those duplicate lines which are adjacent.

10)level 10
password:truKLdjsbJ5g7yyJ2X2R0o3a5HQJFuLk
I just read the file and found the pattern.

11)level 11
password:IFukwKGsFW8MOq3IRFqrxE1hxTNEbUPR
I had decode data using the command (base64 -d data.txt)

12)
password:5Te8Y4drgCRfCx8ugdwuEX8KFC6k2EUu
I decoded rot13 text using the command (echo "Gur cnffjbeq vf 5Gr8L4qetPEsPk8htqjhRK8XSP6x2RHh"|tr ‘n-za-mN-ZA-M’ ‘a-zA-Z’)
