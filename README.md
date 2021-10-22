Skip to content
Search or jump to…
Pull requests
Issues
Marketplace
Explore
 
@HRS05 
HRS05
/
coursera-test
Public
1
00
Code
Issues
Pull requests
Actions
Projects
Wiki
Security
Insights
Settings
coursera-test
/
README.md
in
main
 

Spaces

2

Soft wrap
1
# DOCUMENTATION
2
​
3
## Overview
4
Here you get to know about a `custom javascript library` to avoid the redundancy in programming and also to provide access of commonly used components.
5
​
6
## Why someone use this library ?
7
The main benefits to using to avoid redundancy like if some needs to place an AJAX call so, he/she needs to write the same code, again and again, I also generalized some mainly used components such as Modal, accordion panel and grid.
8
​
9
​
10
* [Ajax calls](#ajax-calls)  
11
   * [Place a call](#place-a-call)
12
   
13
* [Accordion Panel](#accordion-panel)  
14
    * [use of Accordion Panel](#use-of-accordion-panel)
15
* [Modal](#modal)
16
   * [use of Modal](#use-of-modal)
17
* [Grid](#generic-queue)
18
   * [Use of Grid](#use-of-queue-)
19
​
20
## AJAX calls 
21
***
22
Here, we provide functional support for `AJAX` call in which user pass necessary information by wrapping in `JSON` format.  
23
information include : url,methodeType,success and failure.  
24
`url` -> URL for which we want to place an ajax call.   
25
`methodType` -> give the information about request type (default it is of GET type).   
26
`success` -> function execute on successful completion of ajax call.   
27
`failure` -> function execute on failure of ajax call.
28
***
29
### Place a call
30
  ```c
31
$$$.ajax({
32
"url": "requestUrl",
33
"methodType": "GET",
34
"success": function(responseData){
35
​
36
},
37
"failure": function(){
38
​
39
}
40
});
41
  ```
42
## Accordion Panel
43
***
44
To use the accordion panel we need to create a division in which we have to set property `'accordian=true'`, then inside that division, we have to create a heading and below the heading, we have to define respective information whatever we want in the new division just next to it.
No file chosen
Attach files by dragging & dropping, selecting or pasting them.
@HRS05
Commit changes
Commit summary
Create README.md
Optional extended description
Add an optional extended description…
 Commit directly to the main branch.
 Create a new branch for this commit and start a pull request. Learn more about pull requests.
 
© 2021 GitHub, Inc.
Terms
Privacy
Security
Status
Docs
Contact GitHub
Pricing
API
Training
Blog
About
