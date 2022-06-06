# Lab-Report5 Week10

## find the test with different results


I used `vimdiff` to show the differences between the two results but the same test.
Here is the code that I used to show the differences:
```
vimdiff cse15lsp22-markdown-parser/results.txt my-markdown-parser3/results.txt
```
Below is the the output of the results:

<img width="995" alt="Screen Shot 2022-06-05 at 11 57 29 PM" src="https://user-images.githubusercontent.com/103390241/172111325-2d1fe81b-84ac-4d4c-87ea-6bda73cfd92a.png">

<img width="959" alt="Screen Shot 2022-06-05 at 11 57 52 PM" src="https://user-images.githubusercontent.com/103390241/172111340-2798bdc0-d6f2-41a8-90c3-620f85f14d37.png">

<img width="966" alt="Screen Shot 2022-06-05 at 11 58 12 PM" src="https://user-images.githubusercontent.com/103390241/172111356-a32f1e5b-49d1-4b16-8cfa-10770cdfa2e8.png">

Here is the link for the [test-file](https://github.com/nidhidhamnani/markdown-parser/tree/main/test-files)

## Test1

for the test in the 194.md, below is the difference:

<img width="969" alt="Screen Shot 2022-06-06 at 12 06 28 AM" src="https://user-images.githubusercontent.com/103390241/172112420-d0eeaee8-0321-4cb0-8c4f-148dbf0f4cc8.png">

below is the expect output:

<img width="1207" alt="Screen Shot 2022-06-06 at 12 08 36 AM" src="https://user-images.githubusercontent.com/103390241/172112779-f1ce3825-9fe6-4dbd-b3d4-c1585104f74d.png">

It is obivious that two actual outputs are wrong!

The bug happens for the output on the right side because it can not recognize the foobar as a link inside a bracket, since there is one more bracket exist in the two brackets. Since it can not recognize it as a link, it will not give any valid link. That's why there's a bug there.

Below is where should be fixed:

<img width="502" alt="Screen Shot 2022-06-06 at 12 31 00 AM" src="https://user-images.githubusercontent.com/103390241/172115982-7fb27c35-d9c9-4e89-9abf-4c765d32c1d8.png">

It can only recognize the first ending baracket as the link closer, but can not find the link after. However, it should be changed to find the last ending bracket to help find the link.

## Test2

for the test in the 201.md, below is the difference:

<img width="969" alt="Screen Shot 2022-06-06 at 12 11 04 AM" src="https://user-images.githubusercontent.com/103390241/172113088-f760f8ea-f21e-407c-bba2-8c1e9b2cebaa.png">

below is the expect output:

<img width="1170" alt="Screen Shot 2022-06-06 at 12 12 18 AM" src="https://user-images.githubusercontent.com/103390241/172113217-d8421f13-b54e-44b3-93c2-c4a76222a008.png">

Since there's no valid link, so the right output has right answer, but the output on the left doesn't(which is the given repository).

The bug happens on the left becasue it recognizes baz as a link. However baz does not exist in the bracket but in a greater and smaller sign. This should not be happen in the code becasue it can not recognize the value in the <> as a link.

Below is where should be changed:

<img width="598" alt="Screen Shot 2022-06-06 at 12 36 06 AM" src="https://user-images.githubusercontent.com/103390241/172116709-51c062dd-4ce5-4354-8ec1-d4f69ce94de0.png">

Since it only gives the index of the brackets, it also determines the smaller and bigger sign as a potential link, which should not be happened. It needs to be modified by trying to give more limits on dietermine what is a link or no.
