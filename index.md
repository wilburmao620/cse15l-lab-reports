# Remote Access
## Part1: Installing VScode
* Go to the Visual Studio Code website https://code.visualstudio.com/, and follow the instructions and download it.
* Make sure you download the right version of it for the different major operating system, otherwise you will mess it up.
* If you download the right version of it and open it, your screen will look like the image below.
<img width="629" alt="Screen Shot 2022-04-10 at 4 31 05 PM" src="https://user-images.githubusercontent.com/103390241/162646679-2bc97af8-31b4-4e68-ad0c-87948acf9784.png">

## Part2: Remotely Connecting
* Look up your course-specific account for CSE15L: https://sdacs.ucsd.edu/~icc/index.php, and reset the password.
* Open a terminal on the Visual Studio Code((Ctrl + `, or use the Terminal button on the top).
* Enter ssh cs15lsp22zz@ieng6.ucsd.edu (make sure you replace zz by your account letters).
* Enter password for your account.(It is normal if the password doesn't show up)
* Enter Yes and press Enter, if you are the first time log in.
* If you successfully logged in, you will get something in the terminal looked like the image below:
<img width="625" alt="Screen Shot 2022-04-10 at 5 06 46 PM" src="https://user-images.githubusercontent.com/103390241/162646978-4066ce9f-1c7f-4ddb-895c-ea48bd3fad18.png">

## Part3: Run Some Commands
* Try some commands now! Run the commands cd,ls,pwd,mkdir, and cp.
* For example: ls will give you the list of files in the current directory, and pwd will show the directory path.
* Here are some useful commands you may want to try:
  1. cd ~
  2. cd
  3. ls -lat
  4. ls -a
  5. ls <directory>
  6. cp <directory>
  7. cat <directory>
* Try those commands both on your computer and the server computer.
* Here are some examples if you tried pwd and ls:
<img width="626" alt="Screen Shot 2022-04-10 at 5 19 19 PM" src="https://user-images.githubusercontent.com/103390241/162647337-f9a51146-6036-4ff0-9474-ace220c5d32f.png">

  ## Part4: Moving Files with scp
