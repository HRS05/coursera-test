# DOCUMENTATION

## Overview
Here you get to know about a `custom javascript library` to avoid the redundancy in programming and also to provide access of commonly used components.

## Why someone use this library ?
The main benefits to using to avoid redundancy like if some needs to place an AJAX call so, he/she needs to write the same code, again and again, I also generalized some mainly used components such as Modal, accordion panel and grid.


* [Ajax calls](#ajax-calls)  
   * [Place a call](#place-a-call)
   
* [Accordion Panel](#accordion-panel)  
    * [use of Accordion Panel](#use-of-accordion-panel)
* [Modal](#modal)
   * [use of Modal](#use-of-modal)
* [Grid](#generic-queue)
   * [Use of Grid](#use-of-queue-)

## AJAX calls 
***
Here, we provide functional support for `AJAX` call in which user pass necessary information by wrapping in `JSON` format.  
information include : url,methodeType,success and failure.  
`url` -> URL for which we want to place an ajax call.   
`methodType` -> give the information about request type (default it is of GET type).   
`success` -> function execute on successful completion of ajax call.   
`failure` -> function execute on failure of ajax call.
***
### Place a call
  ```c
$$$.ajax({
"url": "requestUrl",
"methodType": "GET",
"success": function(responseData){

},
"failure": function(){

}
});
  ```
## Accordion Panel
***
To use the accordion panel we need to create a division in which we have to set property `'accordian=true'`, then inside that division, we have to create a heading and below the heading, we have to define respective information whatever we want in the new division just next to it.
***
### Use of Accordion Panel
  ```c
  <div accordian='true'>
<h1>Heading 1</h1> 
<div>
</div>

<h1>Heading 2</h1> 
<div>
</div>

<h1>Heading 3</h1> 
<div>
</div>

</div>
  ```

## Modal
***
For creating modal first we need to define some basic properties while creating modal division and also define some pre-required functions.  
following are the properties which required: -
1. division `id`
2. `forModal`='true'
3. `style`
4. `size` (optional)
5. `header` (heading)
6. `footer`
7. `maskColor` (optional)
8. `modalBackgroundColor` (optional)
9. `closeButton` (optional, already set true).

following are the pre-required functions (as property) required:-
1. `beforeOpening` :- the function will execute before opening the modal.
2. `afterOpening` :- the function will execute after opening the modal.
3. `beforeClosing` :- the function will execute before closing the modal.
4. `afterClosing` :- the function will execute after closing the modal.

Note :- for more clarification go for an explanation of how to use modal.
***
### Use of Modal
  ```c
//user written functions
//javascript part

<script>

function abBeforeOpening()
{
alert('ab before opening get called');
return true;
}

function abOpened()
{
alert('Modal with ab opened');
}

function abBeforeClosing()
{
alert('ab before closing get called');
return true;
} 

function abClosed()
{
alert("Modal with ab closed");
}

function createModal()
{
$$$.modals.show("ab");
}
</script>

// html part

<button onCLick='createModal()'>Show First Modal</button>

<div id='ab' style='display:none' forModal='true' size="400X300" header="Some header" footer="Some footer"
 maskColor="#3355ff" modalBackgroundColor="#549933" closeButton="true" beforeOpening="abBeforeOpening()" 
 afterOpening="abOpened()" beforeClosing="abBeforeClosing()" afterClosing="abClosed()">

//content for modal

</div> 
 ```
