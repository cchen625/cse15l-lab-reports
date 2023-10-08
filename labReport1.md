1. cd
~~~
[user@sahara ~/lecture1/messages]$ cd
[user@sahara ~]$ 
~~~
- this was ran when I was inside of the messages folder.
- with no arguments this command doesn't do anything, as it ussually moves you do a desired directory, but with no argument you move no where.
- this isnt an error exactly but it also doesn't do anything.
~~~
[user@sahara ~]$ cd lecture1/messages
~~~
- this line was used inside of the working directory: home.
- when using the argument lecture1/messages the path to the messages directory inside of the first lab, it moved my current directory to messages.
- There were no errors as this was a percectly good thing to do. 
~~~
[user@sahara ~/lecture1/messages]$ cd th.txt
bash: cd: th.txt: Not a directory
~~~
- This line was called from inside of the messages working directory as you can see inside of the code block. 
- Now when I used the cd command on a file inside of the messages folder it bounced back "th.txt: Not a directory" as we can't really make a non directory our current one.
- This was an error as this is not how the cd command is supposed to be used, and it is impossible to treat a file as a directory.

2. ls
~~~
[user@sahara ~/lecture1/messages]$ ls
en-us.txt  es-mx.txt  th.txt  zh-cn.txt
~~~
- this was called inside of the messages working directory.
- Since it was used inside of the messages directory ls simply spit back out all of the files inside of the current directory.
- No errors. 
~~~
[user@sahara ~]$ ls lecture1/messages
en-us.txt  es-mx.txt  th.txt  zh-cn.txt
~~~
- calling the above code inside of the command line from inside of the home working directory, it decieded to once again give me all of the files that are inside of that path.
- No errors. 
~~~
[user@sahara ~/lecture1/messages]$ ls en-us.txt
en-us.txt
~~~
- Calling the above code inside of the command line from inside of the messages working directory, it simply returned back to me the only file that was put it. After trying this with other files the same things occured.
- No errors.

3. cat
~~~
[user@sahara ~/lecture1]$ cat
~~~
- This is what happened when i called cat with no arguments. It simply just went to the next line of the terminal and didn't do anything else.
- I called this from the lecture1 working directory and because of that I suspect that there was nothing in it to readily print out becuase that directory is full of more directories.
- I believe this is an error as afterward I couldn't type more commands into the command line and things seemed to be a little bit messed up as you are supposed to call cat on files.
~~~
[user@sahara ~/lecture1]$ cat messages/en-us.txt
Hello World!
~~~
- called from the working directory lecture1
- no errors occured and as predicted the command made it print out the contents of whatever was inside of the path that I typed out. 
~~~
[user@sahara ~/lecture1]$ cd messages
[user@sahara ~/lecture1/messages]$ cat en-us.txt
Hello World!
~~~
- When calling the function on just the file for en-us.txt, it printed out what was inside of that file to the terminal.
- There were no errors and this was done from the messages directory. 
