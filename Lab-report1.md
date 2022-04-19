# Remote Access
## Part1: Installing VScode
* Go to the Visual Studio Code website [visual studio code](https://code.visualstudio.com/), and follow the instructions and download it.
* Make sure you download the right version of it for the different major operating system, otherwise you will mess it up.
* If you download the right version of it and open it, your screen will look like the image below.
<img width="629" alt="Screen Shot 2022-04-10 at 4 31 05 PM" src="https://user-images.githubusercontent.com/103390241/162646679-2bc97af8-31b4-4e68-ad0c-87948acf9784.png">

## Part2: Remotely Connecting
* Look up your course-specific account for CSE15L: [specifci account](https://sdacs.ucsd.edu/~icc/index.php), and reset the password.
* Open a terminal on the Visual Studio Code((Ctrl + `, or use the Terminal button on the top). 
* Input your specific account, here is the code(make sure you replace zz by your account letters):
```
ssh cs15lsp22zz@ieng6.ucsd.edu
```
* Enter password for your account.(It is normal if the password doesn't show up)
* Enter Yes and press Enter, if you are the first time log in.
* If you successfully logged in, you will get something in the terminal looked like the image below:
<img width="625" alt="Screen Shot 2022-04-10 at 5 06 46 PM" src="https://user-images.githubusercontent.com/103390241/162646978-4066ce9f-1c7f-4ddb-895c-ea48bd3fad18.png">

## Part3: Run Some Commands
* Try some commands now! Run the commands!
* For example: ls will give you the list of files in the current directory, and pwd will show the directory path.
* Here are some useful commands you may want to try:
  ```
  cd ~
  cd
  ls -lat
  ls -a
  ls <directory>
  cp <directory>
  cat <directory>
  pwd
  mkdir
  ```
* Try those commands both on your computer and the server computer, and see what they did.
* Here are some examples if you tried pwd and ls:
<img width="626" alt="Screen Shot 2022-04-10 at 5 19 19 PM" src="https://user-images.githubusercontent.com/103390241/162647337-f9a51146-6036-4ff0-9474-ace220c5d32f.png">

  ## Part4: Moving Files with scp
  * scp is used to copy the file from your computer to the server computer.
  * Create a file on your computer named WhereAmI.java and write some contents in it.
  * In the terminal from the file you made, type in 
  ```
  scp WhereAmI.java cs15lsp22zz@ieng6.ucsd.edu:~/ 
  ```
  (make sure you put your username here).
  * You should need to type in your password for this process, type it in.
  * If you successfully did this, you will get the same file on the server computer.
  * Now, use javac and java command on the ieng6 server computer to see what is happening.
  * You will get something that looks like the image below.
 <img width="630" alt="Screen Shot 2022-04-10 at 5 50 04 PM" src="https://user-images.githubusercontent.com/103390241/162648137-979e2d88-35cd-46be-8990-ab8f7dcb7ce1.png">
  
  ## Part5: Setting an SSH Key
  * SSH key is used to help you do not need to enter password for the ssh anymore!
  * Run the code belown on your computer.
  ```
  ssh-keygen 
  ```
  * It creates two keys: one is public key(in rd_isa.pub), and another is private key(rd_isa). You copy the public key on the server, and the private key on the client.
  * Leave other things blank and keep pressing enter.
  * Copy your public key! Run the code below on your computer and enter your password.
  ```
  ssh cs15lsp22zz@ieng6.ucsd.edu
  ```
  * Run the code below on your server.
  ```
  mkdir .ssh 
  ```
  * Run the code below on the server. (Use your username and the path above)
  ```
  scp /Users/<user-name>/.ssh/id_rsa.pub cs15lsp22zz@ieng6.ucsd.edu:~/.ssh/authorized_keys 
  ```
  * After you success, try scp again! It should not need password anymore!
  * If you success, you should get something that looks like the image below.
 <img width="630" alt="Screen Shot 2022-04-10 at 6 03 06 PM" src="https://user-images.githubusercontent.com/103390241/162648837-5340c955-ebb2-42a9-87ee-cd71bef8998c.png">

  ## Part6: Optimizing Remote Running
  There are many ways to faster your running program.
  * You can use the upper arrow button to repeat the commands what you did before.
  * You can also use the code below to directly run the commands on the server computer.
  ```
  ssh cs15lsp22zz@ieng6.ucsd.edu 
  ```
  * You can use the code below to copy the file directly on the server computer.
  ```
  scp + the directory where you save the file + cs15lsp22zz@ieng6.ucsd.edu
  ```
  * Here is the image of examples, if you try to run your program faster:
  <img width="1367" alt="Screen Shot 2022-04-10 at 6 40 08 PM" src="https://user-images.githubusercontent.com/103390241/162651191-e9abd946-dbe3-466a-94f4-770af83cfec4.png">

