# Lab Report4 Week8

## Links for the repository:
This is the link for my [repository](https://github.com/wilburmao620/markdown-parser.git)

This is the link for I reviewed [repository](https://github.com/calistajlee/lab6-markdown-parser.git)

## Snippet1:
Below is the expected answer:

<img width="356" alt="Screen Shot 2022-05-22 at 6 50 09 PM" src="https://user-images.githubusercontent.com/103390241/169728447-2bda00f5-c1fa-43f3-a5fd-8d0d607de838.png">

Below is how I turned it into the test:

<img width="583" alt="Screen Shot 2022-05-22 at 6 53 33 PM" src="https://user-images.githubusercontent.com/103390241/169728777-bf5f3c3d-351b-4648-b061-79410589acd2.png">

Below is the result that I run the test:

<img width="864" alt="Screen Shot 2022-05-22 at 6 56 24 PM" src="https://user-images.githubusercontent.com/103390241/169729027-0fe738ad-3217-4c32-aa76-9d83e0e5fc61.png">

Below is the result that reviewed run the test:

<img width="760" alt="Screen Shot 2022-05-22 at 7 07 10 PM" src="https://user-images.githubusercontent.com/103390241/169730082-72bfebf9-23d6-41b4-b1bd-06a03f39ad4a.png">

## Snippet2:
Below is the expected answer:

<img width="352" alt="Screen Shot 2022-05-22 at 6 49 44 PM" src="https://user-images.githubusercontent.com/103390241/169728481-a364dae8-f1ee-4271-9c01-cd2bf6b67e1a.png">

Below is how I turned it into the test:

<img width="671" alt="Screen Shot 2022-05-22 at 6 57 48 PM" src="https://user-images.githubusercontent.com/103390241/169729156-af284a05-e241-40ce-9725-8a3899c615ec.png">

Below is the result that I run the test:

<img width="805" alt="Screen Shot 2022-05-22 at 6 59 15 PM" src="https://user-images.githubusercontent.com/103390241/169729299-0b461a8e-9418-46e5-ab46-71e6da0eca08.png">

Below is the result that reviewed run the test:

<img width="802" alt="Screen Shot 2022-05-22 at 7 07 56 PM" src="https://user-images.githubusercontent.com/103390241/169730135-9f738ee0-693a-4878-b42a-159a935d4736.png">

Snippet3:
Below is the expected answer:

<img width="561" alt="Screen Shot 2022-05-22 at 6 51 07 PM" src="https://user-images.githubusercontent.com/103390241/169728553-262b5fe9-3a96-4358-b501-8b4be100714f.png">

Below is how I turned it into the test:

<img width="751" alt="Screen Shot 2022-05-22 at 7 00 40 PM" src="https://user-images.githubusercontent.com/103390241/169729434-d0115073-d775-4d65-846f-35fe5a455349.png">

Below is the result that I run the test:

<img width="875" alt="Screen Shot 2022-05-22 at 7 01 29 PM" src="https://user-images.githubusercontent.com/103390241/169729522-d1f079d2-ab2d-4bbd-bd37-c7ca16de613f.png">

Below is the result that reviewed run the test:

<img width="861" alt="Screen Shot 2022-05-22 at 7 08 35 PM" src="https://user-images.githubusercontent.com/103390241/169730196-d7032d7c-439b-4ed8-8389-d9711d62a51f.png">

## Q&A

1. I think there could be a small change for my code if I want to test it passed. I just need add some lines to be aware of the little backtips infront of the open bracket, so that the whole link will not be counted as valid.
2. For snippet2, I failed at the third case becasue there's another pair of bracket between a bracket. In my code, I regularly count this situation as an abnormal case, so that it will count it as invalid, I will change my code to only recognize the close bracket to end the bracket so that it will consider this situation as a valid input next time. This whole change may take approximately 10 lines.
3. For snippet3, my code recognized the right link but failed at the wrong format. My code gave a result that the end bracket starts a new line, so the only thing I need to do for this situation is to be aware of the format of my answer and make sure I recogize the right ending brackety, and this will take less than 10 lines of code changing.





