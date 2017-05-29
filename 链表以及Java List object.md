# Linked List
### Definition
- A list is consist of a lot nodes
- Each node contain its own value and a reference to the next node
- There are two special nodes, head and tail: head this is first node of the list and tail is the last node of the list.
### 'Reference' concept
- In Java, Object are pass by reference, reference is like the point in C/C++, it tells the JVM where is the object.
### List Operations
- the typical List Operations are 
- 
        add()   //add an element to the list
        delete()    //remove an element from the list
        getNext()   //get the next element from the list
### Single List(单向列表)
- Single List, each node only have one next attribute link itself to the next element.
- Every node is like this:
- 
        class listNode{
            object value; //the is the value contain in the node
            listNode next; //this is the reference to the next node
        }
- Insert operation, delete operation and find operation
### Two End List(双端列表)
- In this list, the head node(header) is different from rest of node, it contain 2 references. one point to the next node, the other point to the tail node.
- The header node should be like this:
- 
        class headNode{
            object value; //the is the value contain in the node
            listNode next; //this is the reference to the next node
            tailNode tail; // this reference connect to the tail node
        }
- Insert operation, delete operation and find operation
### Double List(双向列表)
- For this list, each node in it has two references, one point to the previous node and another point to next node. So it will be effcient to search.
- The node should be like this:
- 
        class doubleListNode{
            object value; //the is the value contain in the node
            doubleListNode next; //this is the reference to the next node
            doubleListNode prev; // this reference connect to the previous node
        }
- Insert operation, delete operation and find operation
### Sorted List(有序列表)
- Sorted List have the same structure of the Single node, but it is sorted. So insert operation will cost more time.
- Insert operation, delete operation and find operation
### Iterator(迭代器)
- Iterator like the header of a list, it contain an reference to its current node, and can get access to this node.
- The structure should be like this:
- 
        class iterator{
            private listNode current; // the reference to the list node we are process now
            public listNode getNext(){} //get the next node
            public boolean hasNext(){} //judge if this list has next node
        }
### Abstract Data Structure(Concept)
- ADT means you do not need to know how the data structure is designed, but you need to know how to use it and its common operations.
- For example, you need to know Stack has pop() and push(), Queue has offer() and poll()
-------
# Java List Object
### List abstract object
- List object in Java is a abstract class, it means you can't get an instance of List class. 
- There are two comman used implemented object, LikedList and ArrayList.
- List class has a generic type constructor, List<T>, you need to specify the object type you want to contain.
- For example:
- 
        List<String> list = new LinkedList<String>();
        List<String> list = new Arraylist<>();
        Stack<String> stack = new LinkedList<String>();
### LinkedList & ArrayList
- In the Java list object, we can use index to get element by get() function. 
### User Define List
- User could easily define a list itself, because we only need to define a attribute belong to this define type named next, we could make it.
- For example:
- 
        class myList{
            int value;
            myList next;
        }
### Iterator
- Java Iterator has two common function, next() and hasNext();
- The common use case is like this:
- 
        while(iter.hasNext()){
            node tmpNode = iter.next();
            // do something with this node
        }        


------