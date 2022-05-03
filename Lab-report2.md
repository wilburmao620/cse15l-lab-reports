# CSE-15l-lab report2
Name: Shibo Mao

Email: s3mao@ucsd.edu
## First Code Change
<img width="1216" alt="Screen Shot 2022-04-24 at 6 27 27 PM" src="https://user-images.githubusercontent.com/103390241/165006359-d3618aa5-4cf9-45d3-a88a-24ce548ffe0b.png">
The symptom is that if there's text after the bracket, it will get into an infinite loop, and never stop. To solve this problem, I set a requirement of stopping the loop, so 
that it will pop out after it reads the text after the bracket.

Here is the failure-inducing input:
<img width="1090" alt="Screen Shot 2022-04-24 at 6 36 04 PM" src="https://user-images.githubusercontent.com/103390241/165006923-45065034-a847-488b-ae7f-c9341a9e588d.png">
Here is the link for test-file [new-test](https://github.com/wilburmao620/markdown-parser/blob/main/new-test.md).

Here is the symptom of the output:

<img width="707" alt="Screen Shot 2022-05-02 at 11 07 35 PM" src="https://user-images.githubusercontent.com/103390241/166410981-050c6027-f80d-41a4-b491-50196aff2e9f.png">


## Second Code Change
<img width="1211" alt="Screen Shot 2022-04-24 at 6 49 34 PM" src="https://user-images.githubusercontent.com/103390241/165007832-76576d1f-ccad-4178-ba46-0cbcc5c1931a.png">
The symptom here shows that it will still read the image link in the test file, but actually it should not read the image as a part of the webpage link. To solve this bug, we should not read the link after the exclamation mark because it is a image link.

Here is the failure-inducing input:
<img width="1085" alt="Screen Shot 2022-04-24 at 6 55 22 PM" src="https://user-images.githubusercontent.com/103390241/165008270-da21d610-54f0-44e8-8d46-c9233bc524ad.png">
Here is the link for test-file[test-file1](https://github.com/wilburmao620/markdown-parser/blob/main/test-file1.md)

## Third Code Change
<img width="1228" alt="Screen Shot 2022-04-24 at 7 09 41 PM" src="https://user-images.githubusercontent.com/103390241/165009312-62e9c815-9ab7-47ce-a6e8-cb26ef624bb8.png">
The symptom here shows that if the link only has bracket but not the parenthesis, and it will not read the invalid input for the link. Before we chenge the code, it will give an infinite loop instead of ignoring the invalid link. After we fix it, it will not read the invalid input anymore.

Here is the failure-inducing input:
<img width="1064" alt="Screen Shot 2022-04-24 at 7 12 38 PM" src="https://user-images.githubusercontent.com/103390241/165009537-01954ab9-022a-450e-a8f5-2c2e5a94e3d9.png">
Here is the link for test-file[test-file](https://github.com/wilburmao620/markdown-parser/blob/main/test-file.md)
