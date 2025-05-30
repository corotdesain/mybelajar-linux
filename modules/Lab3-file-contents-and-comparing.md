# 3 File Contents and Comparing

- [x] 1. Print File Contents (tampilkan ini konten)
- [ ] 2. Display File Contents with Line Numbers (tampilkan ini konten dengan nomor baris)
- [ ] 3. Print the Top Lines of a File
- [ ] 4. View the First Few Bytes of a File
- [ ] 5. Print the Last Lines of a File
- [ ] 6. View the Last Few Bytes of a File
- [ ] 7. Comparing Files
- [ ] 8. Comparing Directories

Objectives __Tujuan__
By the end of this lab, you will be able to:
Pada akhir lab ini, Anda akan dapat:

Use `cat` to display the entire contents of a file
Use `head` to view the beginning of a file
Use `tail` to view the end of a file
Use `diff` to compare the contents of files and directories
<hr>

- [x] 1. Print File Contents  
labex:project/ $ cat /tmp/hello  
    ```  
    Hi,
    I am Labby!
    ```  
- [x] 2. Display File Contents with Line Numbers  

labex:project/ $ cat -n /tmp/hello  
     ```  
     1  Hi,
     2  I am Labby!  
     ```  
     Here, -n1 is an option that tells head to show only the first line. The 1 can be changed to any number to show that many lines.  
- [x] 3. Print the Top Lines of a File  
labex:project/ $ head -n1 /tmp/hello  
```
Hi,
```  
This is just the first line of the file. By default, without the -n1 option, head would show the first 10 lines of the file.  
- [x] 4. View the First Few Bytes of a File
      labex:project/ $ head -c1 /tmp/hello
The -c1 option tells head to show only the first byte (character) of the file. Like with -n, you can change the 1 to any number to see that many bytes.
```
H
```
This is just the first character of the file. In text files, each character is typically one byte.

- [x] 5. Print the Last Lines of a File
      labex:project/ $ tail -n1 /tmp/hello
      Just like with head, the -n1 option tells tail to show only one line, in this case the last line of the file.  
```
      I am Labby!
```
This is the last line of our file. Without the -n1 option, tail would show the last 10 lines by default.
- [x] 6. View the Last Few Bytes of a File
   `tail -c1 /tmp/hello`
```

```
You might not see any output. This is because the last character is likely a newline character, which is invisible.

   `tail -c2 /tmp/hello`
```
!
```
  The -c2 option tells tail to show the last 2 bytes (characters) of the file. In this case, it's showing the exclamation mark, which is the last visible character in our file.
- [x] 7. Comparing Files
      First, let's make sure we're in the right directory (folder). Type the following command and press Enter:
      `cd ~` atau `cd $HOME`  
   
    `diff file1 file2`  

    This tells diff to compare the contents of file1 and file2.  

     ```
     1c1
    < this is file1
    ---
    > this is file2
     ```  
This output is telling us that line 1 of file1 is different from line 1 of file2. The < symbol shows the content from file1, and the > symbol shows the content from file2.
     
- [ ] 8. Comparing Directories  
        Finally, let's use the diff command to compare entire directories.  
      `diff -r ~/Desktop ~/Code`  
      The -r option tells diff to recursively compare subdirectories as well. ~/Desktop and ~/Code are the paths to the two directories we're comparing.

```  
Only in /home/labex/Desktop: code.desktop
Only in /home/labex/Desktop: gedit.desktop
Only in /home/labex/Desktop: gvim.desktop
Only in /home/labex/Desktop: xfce4-terminal.desktop
```
This output shows that the Desktop directory contains four files that are not in the Code directory.    


<h3> Summary </h3>
Congratulations! You've completed the File Contents and Comparing lab. Let's recap what you've learned:  

1 You used cat to view the entire contents of a file.  
2 You learned how to use cat -n to view file contents with line numbers.  
3 You used head to view the beginning of a file, both by lines and by bytes.  
4 You used tail to view the end of a file, both by lines and by bytes.  
5 You learned how to use diff to compare the contents of files.  
6 Finally, you used diff -r to compare entire directories.  
These commands are fundamental tools in Linux. As you continue to work with Linux, you'll find yourself using these commands frequently to inspect and compare files and directories.  

Remember, if you ever forget how to use a command, you can always type man followed by the command name (e.g., man cat) to see the manual page for that command. This will give you detailed information about all the options available for each command.  

Keep practicing with these commands on different files and directories to become more comfortable with them. The more you use them, the more natural they'll become!  
