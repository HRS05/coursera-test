# DOCUMENTATION

* [Singly Linked List](#singly-linked-list)  
   * [Singly Linked List Iterator](#description-of-iterator-fuctions-)
* [Doubly Linked Linked](#doubly-linked-list)  
   * [Doubly Linked List Iterator](#description-of-iterator-fuctions-)
* [Stack](#stack)
* [Queue](#queue)

## Singly Linked List  
***
### Description of Main functions :

* To `create` SinglyLinkedList
   ```c
   SinglyLinkedList * createSinglyLinkedList(bool *success); 
   ```
   `bool success;`  
    `SinglyLinkedList *list;`  
    `list=createSinglyLinkedList(&success);`  
    if(`success==true`) list created.  
    if(`success==false`) list is not created.  

* To `add` element in Singly Linked List
  ```c
  void addToSinglyLinkedList(SinglyLinkedList *singlyLinkedList,void *ptr,bool *success);
  ```
  `bool success;`  
  `int i=100;`  
  `addToSinglyLinkedList(list,(void *)&i,&success);`  
   if(`success==true`) element is added.  
   if(`success==false`) element is not added.  
    
* To `insert` element in Singly Linked List
   ```c
   void insertIntoSinglyLinkedList(SinglyLinkedList *singlyLinkedList,int index,void *ptr,bool *success);
   ```
  `bool success;`  
  `int i=100;`  
  `int index;` (position to insert element in list)  
  `insertIntoSinglyLinkedList(list,index,(void *)&i,&success);`  
   if(`success==true`) element is inserted.  
   if(`success==false`) element is not   inserted.  
   
* To `remove` element in Singly Linked List
  ```c
  void * removeFromSinglyLinkedList(SinglyLinkedList *singlyLinkedList,int index,bool *success);
  ```
  funtion will return removed element's information.
  `bool success;`  
  `void * ptr;`  
  `int index;` (position to remove element in list)  
  `ptr=removeFromSinglyLinkedList(list,index,&success);`  
  if(`success==true`) element is removed.  
  if(`success==false`) element is not removed.  

* To `get size` of Singly Linked List
  ```c
  int getSizeOfSinglyLinkedList(SinglyLinkedList *singlyLinkedList);
  ```
  `int size;`  
  `size=getSizeOfSinglyLinkedList(list);`  
* To `get an element` from Singly Linked List  
  ```c
  void * getFromSinglyLinkedList(SinglyLinkedList *singlyLinkedList,int index,bool *success);
  ```
  `bool success;`  
  `void * ptr;`  
  `int index;`  
  `ptr=getFromSinglyLinkedList(list,index,&success);`  
  if(`success==true`) element is received in ptr.  
  if(`success==false`) element is not received int ptr.  

* To `merge one list into another list` of Singly Linked List  
  ```c
  void appendToSinglyLinkedList(SinglyLinkedList *targetSinglyLinkedList,SinglyLinkedList * sourceSinglyLinkedList,bool *success);
  ```
  we have `list_1` and `list_2` of SinglyLinkedList.  
  for merging `list_1` into `list_2`.  
  `bool success;`   
  `appendToSinglyLinkedList(list_1,list_2,&success);`  
  if(`success==true`) lists are merged.  
  if(`success==false`) lists are not merged.  

* To `clear` the Singly Linked List  
  ```c
  void clearSinglyLinkedList(SinglyLinkedList *singlyLinkedList);
  ```
  use to make list nodes free (size of list is zero).  
  `clearSinglyLinkedList(list);`  
* To `delete/destroy` the Singly Linked List    
  ```c
  void destroySinglyLinkedList(SinglyLinkedList *singlyLinkedList);
  ```
  use to delete the list.  
  `destroySinglyLinkedList(list);`  
  ***  
### Description of Iterator fuctions :  

* To `create iterator` of Singly Linked List
  ```c
  SinglyLinkedListIterator getSinglyLinkedListIterator(SinglyLinkedList *singlyLinkedList,bool *success);
  ```
  `DoublyLinkedListIterator it;`      
  `bool success;`  
  `it=getsinglyLinkedListIterator(list,&success);`  
  if(`success=true`) iterator (it) is created.  
  if(`success==false`) iterator (it) is not created.  
  
* To `check iterator's position` in Singly Linked List
  ```c
  bool hasNextInSinglyLinkedList(SinglyLinkedListIterator *singlyLinkedListIterator);   
  ```
  `bool check;`  
  `check=hasNextInSinglyLinkedList(&it);`  
  if(`check==true`) next element is exist in the list.  
  if(`check==false`) iterator is at end of the list.  

* To `check iterator's position` in Singly Linked List  
  ```c
  void * getNextElementFromSinglyLinkedList(SinglyLinkedListIterator *singlyLinkedListIterator,bool *success);  
  ```
  In this funtion iterator will return the current pointing element (data of node) and traverse one step forward.  
  `void * ptr;`  
  `bool success;`  
  `ptr=getNextElementFromSinglyLinkedList(&it,&success);`  
  if(`success=true`) element is received in ptr.  
  if(`success=false`)  element is not received in ptr.  
  
  ***


## Doubly Linked List
***
### Description of Main fuctions :

* To `create` DoublyLinkedList
   ```c
   DoublyLinkedList * createDoublyLinkedList(bool *success); 
   ```
   `bool success;`  
    `DoublyLinkedList *list;`  
    `list=createDoublyLinkedList(&success);`   
    if(`success==true`) list created.    
    if(`success==false`) list is not created.  

* To `add` element in Doubly Linked List
  ```c
  void addToDoublyLinkedList(DoublyLinkedList *doublyLinkedList,void *ptr,bool *success);
  ```
  `bool success;`  
  `int i=100;`  
  `addToDoublyLinkedList(list,(void *)&i,&success);`  
   if(`success==true`) element is added.  
   if(`success==false`) element is not added.  
    
* To `insert` element in Doubly Linked List
   ```c
   void insertIntoDoublyLinkedList(DoublyLinkedList *doublyLinkedList,int index,void *ptr,bool *success);  
   ```
  `bool success;`  
  `int i=100;`  
  `int index;` (position to insert element in list)  
  `insertIntoDoublyLinkedList(list,index,(void *)&i,&success);`  
   if(`success==true`) element is inserted.  
   if(`success==false`) element is not inserted.  
   
* To `remove` element in Doubly Linked List  
  ```c
  void * removeFromDoublyLinkedList(DoublyLinkedList *doublyLinkedList,int index,bool *success);  
  ```
  funtion will return removed element's information.  
  `bool success;`  
  `void * ptr;`  
  `int index;` (position to remove element in list)  
  `ptr=removeFromDoublyLinkedList(list,index,&success);`  
  if(`success==true`) element is removed.  
  if(`success==false`) element is not removed.  

* To `get size` of Doubly Linked List
  ```c
  int getSizeOfDoublyLinkedList(DoublyLinkedList *doublyLinkedList);  
  ```
  `int size;`  
  `size=getSizeOfDoublyLinkedList(list);`  

* To `get an element` from Doubly Linked List    
  ```c
  void * getFromDoublyLinkedList(DoublyLinkedList *doublyLinkedList,int index,bool *success);
  ```
  `bool success;`  
  `void * ptr;`  
  `int index;`  
  `ptr=getFromDoublyLinkedList(list,index,&success);`  
  if(`success==true`) element is received in ptr.  
  if(`success==false`) element is not received int ptr.  

* To `merge one list into another list` of Doubly Linked List  
  ```c
  void appendToDoublyLinkedList(DoublyLinkedList *targetDoublyLinkedList,DoublyLinkedList * sourceDoublyLinkedList,bool *success);
  ```
  we have `list_1` and `list_2` of DoublyLinkedList.    
  for merging `list_1` into `list_2`.  
  `bool success;`  
  `appendToDoublyLinkedList(list_1,list_2,&success);`  
  if(`success=true`) lists are merged.  
  if(`success==false`) lists are not merged.  

* To `clear` the Doubly Linked List  
  ```c
  void clearDoublyLinkedList(DoublyLinkedList *doublyLinkedList);
  ```
  use to make list nodes free (size of list is zero).  
  `clearDoublyLinkedList(list);`

* To `delete/destroy` the Doubly Linked List    
  ```c
  void destroyDoublyLinkedList(DoublyLinkedList *doublyLinkedList);
  ```
  use to delete the list.  
  `destroyDoublyLinkedList(list);`  
  ***
### Description of Iterator fuctions :

* To `create iterator` of Doubly Linked List
  ```c
  DoublyLinkedListIterator getDoublyLinkedListIterator(DoublyLinkedList *doublyLinkedList,bool *success);  
  ```
  `DoublyLinkedListIterator it;`  
  `bool success;`  
  `it=getdoublyLinkedListIterator(list,&success);`  
  if(`success=true`) iterator (it) is created.  
  if(`success==false`) iterator (it) is not created.  
  
* To `check iterator's position` in Doubly Linked List
  ```c
  bool hasNextInDoublyLinkedList(DoublyLinkedListIterator *doublyLinkedListIterator); 
  ```
  `bool check;`  
  `check=hasNextInDoublyLinkedList(&it);`  
  if(`check==true`) next element is exist in the list.  
  if(`check==false`) iterator is at end of the list.  

* To `check iterator's position` in Doubly Linked List
  ```c
  void * getNextElementFromDoublyLinkedList(DoublyLinkedListIterator *doublyLinkedListIterator,bool *success);
  ```
  In this funtion iterator will return the current pointing element (data of node) and traverse one step forward.  
  `void * ptr;`  
  `bool success;`  
  `ptr=getNextElementFromDoublyLinkedList(&it,&success);`  
  if(`success=true`) element is received in ptr.  
  if(`success=false`)  element is not received in ptr.  

* To `create reverse iterator` of Doubly Linked List
  ```c
  DoublyLinkedListReverseIterator getDoublyLinkedListReverseIterator(DoublyLinkedList *doublyLinkedList,bool *success);
  ```
  `DoublyLinkedListReverseIterator it;`
  `bool success;`  
  `it=getdoublyLinkedListIterator(list,&success);`  
  if(`success=true`) reverse iterator (it) is created.  
  if(`success==false`) reverse iterator (it) is not created.  
  
* To `check reverse iterator's position` in Doubly Linked List
  ```c
  bool hasPreviousInDoublyLinkedList(DoublyLinkedListReverseIterator *doublyLinkedListReverseIterator); 
  ```
  `bool check;`  
  `check=hasPreviousInDoublyLinkedList(&it);`  
  if(`check==true`) previous element is exist in the list.  
  if(`check==false`) iterator is at start of the list.  

* To `check reverse iterator's position` in Doubly Linked List
  ```c
  void * getPreviousElementFromDoublyLinkedList(DoublyLinkedListReverseIterator *doublyLinkedListReverseIterator,bool *success);
  ```
  In this funtion iterator will return the current pointing element (data of node) and traverse one step backward.  
  `void * ptr;`  
  `bool success;`  
  `ptr=getPreviousElementFromDoublyLinkedList(&it,&success);`  
  if(`success=true`) element is received in ptr.  
  if(`success=false`)  element is not received in ptr.  
  

## Stack



## Queue

