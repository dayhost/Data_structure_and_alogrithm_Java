# Queue & Stack
### The definition of Queue and Stack
- The keyword for Queue is FIFO, means 'first in, first out'. It should provide two operations: add(element),poll(). 'add' function could add an element into the tail of the queue and 'poll' function will get the element in the head. For example:
- 
        add 1, 2, 3, 4, 5 into the Queue
        poll 5 times, we could get: 1, 2, 3, 4, 5
- The keyword for Stack is FILO, means 'first in, last out'. It should provide two operations: push(element) and pop(). 'push' function could add an element into the top of the stack, and 'pop' function could get the top element from the stack. For example:
- 
        push 1 ,2 ,3 ,4 ,5 into the stack
        pop 5 times, we could get: 5, 4, 3, 2, 1
### Queue and Stack in Java
- Java provide Queue and Stack in java.util package. It also provide standard operations for those two structure. However, we need to told java what type we want to store in it. For example:
- 
        Queue<Integer> or Queue<String> or Queue<Boolean>
        Stack<Integer> or Stack<String> or Stack<Boolean>
--------
# Java Object Oriented Design
### [1]abstract & interface
- abstract: this keyword could apply to class or function. For example:
- 
        abstract class MyAbstractClass{
            abstract void function(){}
            void realfunction(){
                //do something
            }
        }
- Abstract class must have one or more abstruct functions. This abstract function has no code in it, just the name, input and output.
- We need to use implement keyword to inherit this class and override and implement the abstract function.
- interface: this keyword could only apply to class. For example:
- 
        interface MyInterfaceClass{
            void function1(){}
            int function2(int num){}
        }
- All the function in interface have no code in it, just name, input and output.
- 'interface' also need to use implement to inherit.
- The different between interface and abstract is that abstract could have implemented function but interface could not.
### [2]extends & implement
- 'extends' keyword could not use for abstract or interface. But it can work for other classes.
- 'implement' keyword could apply to abstract and interface, like this:
- 
        // for interface
        class sampleClass1 implement MyInterfaceClass{
            @Override
            void function1(){
                //do something
            }
            @Override
            int function2(int num){
                //do something
            }
        }
        //for abstract
        class sampleClass2 implement MyAbstractClass{
            @Override
            void function(){
                //do something
            }
        }
### [3]enum(枚举类)
- Enum keyword is use for list values we need to use, for example:
- 
        enum MyEnumClass{
            One,Two,Three,Four
        }
- In this class, it only has 4 values, we can get access to the value by：
- 
        MyEnumClass.One;
### [4]public & private & protect
- 'public' keyword means it can be accessed from all the outside class.
- 'private' keyword means it can only be accessed by the current class.
- 'protect' keyword means it can be accessed by current class and other classes that inherit this class.
-------
# Let's try some thing with what we have known
### Implement Queue using Stacks (LeetCode 232)
    public class MyQueue {
    
        Stack<Integer> in;
        Stack<Integer> out;
    
        /** Initialize your data structure here. */
        public MyQueue() {
            in = new Stack<Integer>();
            out = new Stack<Integer>();
        }
        
        /** Push element x to the back of queue. */
        public void push(int x) {
            in.push(x);
        }
        
        /** Removes the element from in front of queue and returns that element. */
        public int pop() {
            if(out.isEmpty()){
                while(!in.isEmpty()){
                    out.push(in.pop());
                }
            }
            return out.pop();
        }
        
        /** Get the front element. */
        public int peek() {
            if(out.isEmpty()){
                while(!in.isEmpty()){
                    out.push(in.pop());
                }
            }
            return out.peek();
        }
        
        /** Returns whether the queue is empty. */
        public boolean empty() {
            return in.isEmpty()&&out.isEmpty();
        }
    }
### Implement Stack using Queues (LeetCode 225)
    public class MyStack {

        Queue<Integer> stack;
        
        /** Initialize your data structure here. */
        public MyStack() {
            stack = new LinkedList<Integer>();
        }
        
        /** Push element x onto stack. */
        public void push(int x) {
            stack.offer(x);
            for(int i=0; i<stack.size()-1; i++){
                int tmp = stack.poll();
                stack.offer(tmp);
            }
        }
        
        /** Removes the element on top of the stack and returns that element. */
        public int pop() {
            return stack.poll();
        }
        
        /** Get the top element. */
        public int top() {
            return stack.peek();
        }
        
        /** Returns whether the stack is empty. */
        public boolean empty() {
            return stack.isEmpty();
        }
    }
