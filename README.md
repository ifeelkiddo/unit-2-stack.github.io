<!doctype html>
<html>
<head>
  <meta http-equiv="content-type" content="text/html; charset=utf-8">
  <title>unit 2</title>
  <meta name="generator" content="CherryTree">
  <link rel="stylesheet" href="res/styles4.css" type="text/css" />
</head>
<body>
<div class='page'><h1 class='title'>unit 2</h1><br/><p></p><p><strong><h2>Module 2:</h2></strong><span style="indent:1;"></span></p><p><span style="indent:1;"></span><strong><span style="color:#9400ff;">Stacks: Stacks as ADT, Different implementation of stack, multiple stacks. Application of Stack: Conversion of infix to postfix notation using stack, evaluation of postfix expression, Recursion. Queues Queues as ADT, Different implementation of queue, Circular queue,  Concept of Dqueue and Priority Queue, Queue simulation, Application of queues. </span></strong><span style="color:#9400ff;"></span></p><p><span style="color:#9400ff;"></span></p><p><strong><h2>STACK</h2></strong></p><p></p><p><strong><h2>What is Stack Data Structure?</h2></strong></p><p><strong><h3>Stack </h3></strong><h3>is a </h3><strong><h3>linear data structure </h3></strong><h3>based on LIFO(Last In First Out) principle in which the insertion of a new element and removal of an existing element takes place at the same end represented as the </h3><strong><h3>top </h3></strong><h3>of the stack. </h3><h3>To implement the stack, it is required to maintain the </h3><strong><h3>pointer to the top of the stack </h3></strong><h3>, which is the last element to be inserted because </h3><strong><h3>we can access the elements only on the top of the stack.</h3></strong><h3> </h3></p><p></p><p></p><p><strong><h2>Types of Stack Data Structure:</h2></strong><h2></h2></p><p><h2></h2><ul><li><span style="text-decoration:underline;">• </span><h3>• </h3><strong><h3>Fixed Size Stack </h3></strong><h3>: </h3><h3>As the name suggests, a fixed size stack has a fixed size and cannot grow or shrink dynamically. If the stack is full and an attempt is made to add an element to it, an overflow error occurs. If the stack is empty and an attempt is made to remove an element from it, an underflow error occurs</h3><h3>.</h3></li><li><h2>• </h2><h3>• </h3><strong><h3>Dynamic Size Stack </h3></strong><h3>: </h3><h3>A dynamic size stack can grow or shrink dynamically. When the stack is full, it automatically increases its size to accommodate the new element, and when the stack is empty, it decreases its size. This type of stack is implemented using a linked list, as it allows for easy resizing of the stack.</h3></li></ul><h2></h2></p><p><h2></h2><h2></h2></p><p><h2></h2><h2>Basic Operations on</h2><strong><h2> Stack Data Structure:</h2></strong></p><p></p><p></p><p><strong><h2>Push Operation</h2></strong></p><p><h3>Adds an item to the stack. If the stack is full, then it is said to be an </h3><strong><h3>Overflow condition.</h3></strong><ul><li>• <h3>• Before pushing the element to the stack, we check if the stack is </h3><strong><h3>full </h3></strong><h3>.</h3></li><li>• <h3>• If the stack is full </h3><strong><h3>(top == capacity-1) </h3></strong><h3>, then </h3><strong><h3>Stack Overflows </h3></strong><h3>and we cannot insert the element to the stack.</h3></li><li>• <h3>• Otherwise, we increment the value of top by 1 </h3><strong><h3>(top = top + 1) </h3></strong><h3>and the new value is inserted at </h3><strong><h3>top position </h3></strong><h3>.</h3></li><li>• <h3>• The elements can be pushed into the stack till we reach the </h3><strong><h3>capacity </h3></strong><h3>of the stack.</h3></li></ul></p><p></p><p><img src="images/16-1.png" alt="images/16-1.png" /></p><p></p><p><strong><h2>Pop Operation in Stack Data Structure:</h2></strong></p><p><h3>Removes an item from the stack. The items are popped in the reversed order in which they are pushed. If the stack is empty, then it is said to be an </h3><strong><h3>Underflow condition.</h3></strong></p><p><strong><h2>Algorithm for Pop Operation:</h2></strong><ul><li>• <h3>• Before popping the element from the stack, we check if the stack is </h3><strong><h3>empty </h3></strong><h3>.</h3></li><li>• <h3>• If the stack is empty (top == -1), then </h3><strong><h3>Stack Underflows </h3></strong><h3>and we cannot remove any element from the stack.</h3></li><li>• <h3>• </h3><h3> Otherwise, we store the value at top, decrement the value of top by 1 </h3><strong><h3>(top = top – 1) </h3></strong><h3>and return the stored top value.</h3></li></ul></p><p>•</p><p> <img src="images/16-2.png" alt="images/16-2.png" /></p><p></p><p><strong><h2>Top or Peek Operation in Stack Data Structure:</h2></strong></p><p><h3>Returns the top element of the stack.</h3></p><p><strong><h2>Algorithm for Top Operation:</h2></strong><ul><li>• <h3>• Before returning the top element from the stack, we check if the stack is empty.</h3></li><li>• <h3>• If the stack is empty (top == -1), we simply print “Stack is empty”.</h3></li><li>• <h3>• Otherwise, we return the element stored at </h3><strong><h3>index = top </h3></strong><h3>.</h3></li></ul></p><p></p><p><img src="images/16-3.png" alt="images/16-3.png" /></p><p></p><p><strong><h2>isEmpty Operation in Stack Data Structure:</h2></strong></p><p><h3>Returns true if the stack is empty, else false.</h3></p><p><strong><h2>Algorithm for isEmpty Operation</h2></strong><h2>:</h2><ul><li>• <h3>• Check for the value of </h3><strong><h3>top </h3></strong><h3>in stack.</h3></li><li>• <h3>• If </h3><strong><h3>(top == -1) </h3></strong><h3>, then the stack is </h3><strong><h3>empty </h3></strong><h3>so return </h3><strong><h3>true </h3></strong><h3>.</h3></li><li>• <h3>• Otherwise, the stack is not empty so return </h3><strong><h3>false </h3></strong><h3>.</h3></li></ul></p><p></p><p><img src="images/16-4.png" alt="images/16-4.png" /></p><p></p><p><h2>isFull </h2><strong><h2>Operation in Stack</h2></strong><h2> </h2><strong><h2>Data Structure</h2></strong><h2>:</h2></p><p><h3>Returns true if the stack is full, else false.</h3></p><p><strong><h2>Algorithm for isFull Operation:</h2></strong><ul><li>• <h3>• Check for the value of </h3><strong><h3>top </h3></strong><h3>in stack.</h3></li><li>• <h3>• If </h3><strong><h3>(top == capacity-1), </h3></strong><h3>then the stack is </h3><strong><h3>full </h3></strong><h3>so return </h3><strong><h3>true</h3></strong><h3>.</h3></li><li>• <h3>• Otherwise, the stack is not full so return </h3><strong><h3>false</h3></strong><h3>.</h3></li></ul></p><p></p><p><img src="images/16-5.png" alt="images/16-5.png" /></p><p></p><p></p><p><h2>Implementation of Stack </h2><strong><h2>Data Structure</h2></strong><h2>:</h2></p><p><h3>The basic operations that can be performed on a stack include push, pop, and peek. There are two ways to implement a stack –</h3><ul><li>• <strong><h3>• </h3></strong><h3>Using</h3><strong><h3> Array</h3></strong></li><li><strong>• </strong><strong><h3>• </h3></strong><h3>Using</h3><strong><h3> Linked List</h3></strong></li></ul></p><p></p><p><strong><h2>Implementation of Stack Data Structure using Array:</h2></strong></p><p></p><p><div class="codebox"><pre><span style="color:#a020f0;font-weight:400">#include&lt;stdio.h&gt;</span><br /><br /><span style="color:#0000ff;font-weight:400">//impementation with array</span><br />Class Stack<br /> {<br />  <span style="color:#2e8b57;font-weight:700">int</span> *arr;<br />  <span style="color:#2e8b57;font-weight:700">int</span> size;<br />  <span style="color:#2e8b57;font-weight:700">int</span> top;<br /><br />  Public:<br />   stack( <span style="color:#2e8b57;font-weight:700">int</span> s )<br />   size=s;<br />   top=-<span style="color:#ff00ff;font-weight:400">1</span>;<br />   arr= <span style="color:#a52a2a;font-weight:700">new</span> <span style="color:#2e8b57;font-weight:700">int</span>[s];<br /><br /><span style="color:#0000ff;font-weight:400">//first function (PUSH)</span><br /><br /> <span style="color:#2e8b57;font-weight:700">void</span> push(<span style="color:#2e8b57;font-weight:700">int</span> value)<br />  <span style="color:#a52a2a;font-weight:700">if</span>(top==size-<span style="color:#ff00ff;font-weight:400">1</span>)<br />   {<br />   cout &lt;&lt; <span style="color:#ff00ff;font-weight:400">&quot;Stack Overflow&quot;</span>;<br /><br />   <span style="color:#a52a2a;font-weight:700">return</span>;<br />   }<br /><br />  <span style="color:#a52a2a;font-weight:700">else</span><br />   {<br />   top++<br />   arr[top] = value<br />   cout&lt;&lt;<span style="color:#ff00ff;font-weight:400">&quot;Pushed &quot;</span>&lt;&lt;value&lt;&lt;<span style="color:#ff00ff;font-weight:400">&quot;into the stack\n&quot;</span><br />   }<br /><span style="color:#2e8b57;font-weight:700">void</span> pop()<br />  <span style="color:#a52a2a;font-weight:700">if</span>(top==-<span style="color:#ff00ff;font-weight:400">1</span>)<br />   {<br />   cout &lt;&lt; <span style="color:#ff00ff;font-weight:400">&quot;stack overflow&quot;</span>;<br />   }<br /></pre></div></p><p></p><p><h2>Advantages of Array Implementation:</h2><ul><li>• <h3>• Easy to implement.</h3></li><li>• <h3>• Memory is saved as pointers are not involved.</h3></li></ul></p><p></p><p><h2>Disadvantages of Array Implementation:</h2><ul><li>• <h3>• It is not dynamic i.e., it doesn’t grow and shrink depending on needs at runtime. [But in case of dynamic sized arrays like vector in C++, list in Python, ArrayList in Java, stacks can grow and shrink with array implementation as well].</h3></li><li>• <h3>• The total size of the stack must be defined beforehand.</h3></li></ul></p><p></p><p></p><p><strong><h2>Implementation of Stack Data Structure using Linked List:</h2></strong></p><p></p><p><h2>Advantages of Linked List implementation:</h2><ul><li>• <h3>• The linked list implementation of a stack can grow and shrink according to the needs at runtime.</h3></li><li>• <h3>• It is used in many virtual machines like JVM.</h3></li></ul></p><p></p><p><h2>Disadvantages of Linked List implementation:</h2><ul><li>• <h3>• Requires extra memory due to the involvement of pointers.</h3></li><li>• <h3>•  Random accessing is not possible in stack.</h3></li></ul></p><p></p><p></p><p><strong><h2>Complexity Analysis of Operations on Stack Data Structure:</h2></strong></p><p><table class="table"><tr><th>Operations</th><th>Time Complexity</th><th>Space Complexity</th></tr><tr><td>push()</td><td>O(1)</td><td>O(1)</td></tr><tr><td>pop()</td><td>O(1)</td><td>O(1)</td></tr><tr><td>top() or peek()</td><td>O(1)</td><td>O(1)</td></tr><tr><td>isEmpty()</td><td>O(1)</td><td>O(1)</td></tr><tr><td>isFull()</td><td>O(1)</td><td>O(1)</td></tr></table></p><p></p><p><h2>Advantages of Stack </h2><strong><h2>Data Structure</h2></strong><h2>:</h2><ul><li>• <h3>• </h3><strong><h3>Simplicity: </h3></strong><h3>Stacks are a simple and easy-to-understand data structure, making them suitable for a wide range of applications.</h3></li><li><strong>Efficiency: </strong><h3>Push and pop operations on a stack can be performed in constant time </h3><strong>(O(1)) </strong><h3>, providing efficient access to data.</h3></li><li>• <h4>• </h4><strong><h4>Last-in, First-out (LIFO): </h4></strong><h4>Stacks follow the LIFO principle, ensuring that the last element added to the stack is the first one removed. This behavior is useful in many scenarios, such as function calls and expression evaluation.</h4></li><li><strong>Limited memory usage: </strong><h3>Stacks only need to store the elements that have been pushed onto them, making them memory-efficient compared to other data structures.</h3></li></ul></p><p></p><p></p><p><h2>Disadvantages of Stack </h2><strong><h2>Data Structure</h2></strong><h2>:</h2><ul><li><strong>Limited access: </strong><h3>Elements in a stack can only be accessed from the top, making it difficult to retrieve or modify elements in the middle of the stack.</h3></li><li><strong>Potential for overflow: </strong><h3>If more elements are pushed onto a stack than it can hold, an overflow error will occur, resulting in a loss of data.</h3></li><li><strong>Not suitable for random access: </strong><h3>Stack</h3><strong><span style="text-decoration:underline;"> </span></strong><h3>s do not allow for random access to elements, making them unsuitable for applications where elements need to be accessed in a specific order.</h3></li><li><strong>Limited capacity: </strong><h3>Stacks have a fixed capacity, which can be a limitation if the number of elements that need to be stored is unknown or highly variable.</h3></li></ul></p><p></p><p></p><p><strong><h2>Applications of Stack Data Structure:</h2></strong><ul><li><h3>Infix to Postfix /Prefix conversion</h3></li><li><h3>Redo-undo features at many places like editors, photoshop.</h3></li><li><h3>Forward and backward features in web browsers</h3></li><li><h3>In Memory management, any modern computer uses a stack as the primary management for a running purpose. Each program that is running in a computer system has its own memory allocations.</h3></li><li><h3>Stack also helps in implementing function call in computers. The last called function is always completed first.</h3></li></ul></p><p></p><p><strong><h2>Queue</h2></strong><h2> Data Structure</h2><strong><h2>:</h2></strong></p><p></p><p><h3>Queue Dat Structure is a linear Data structure that follows</h3><strong><h3> FIFO (First In First Out) Principle</h3></strong><h3>, so the first element inserted is the first to be popped out.</h3><img src="images/16-6.png" alt="images/16-6.png" /></p><p></p><p></p><p><strong><h2>Types of Queues:</h2></strong></p><p></p><p><img src="images/16-7.png" alt="images/16-7.png" /></p><p></p><p><h3>There are</h3><strong><h3> five different types of queues</h3></strong><h3> that are used in different scenarios. They are:</h3><ol><li>Circular Queue</li><li>Output Restricted Queue (this is also a Simple Queue)</li><li>Input Restricted Queue (this is a Simple Queue)</li><li>Double Ended Queue (Deque)</li><li>Priority Queue</li><li>• <span style="indent:1;">• Ascending Priority Queue</span></li><li><span style="indent:1;">Descending Priority Queue</span></li></ol></p><p></p><p><strong><h2>Circular Queue:</h2></strong><span style="color:#002986;"></span></p><p><span style="color:#002986;"></span><h3>Circular Queue is a linear data structure in which the operations are performed based on FIFO (First In First Out) principle and the last position is connected back to the first position to make a circle. It is also called </h3><strong><h3>‘Ring Buffer’</h3></strong><span style="color:#002986;"></span></p><p><span style="color:#002986;"></span><img src="images/16-8.png" alt="images/16-8.png" /></p><p></p><p><strong><h2>Operations on Circular Queue:</h2></strong><ul><li>• <h3>• </h3><strong><h3>Front:</h3></strong><h3> Get the front item from the queue.</h3></li><li>• <h3>• </h3><strong><h3>Rear:</h3></strong><h3> Get the last item from the queue.</h3></li><li>• <h3>• </h3><strong><h3>enQueue(value) </h3></strong><h3>This function is used to insert an element into the circular queue. In a circular queue, the new element is always inserted at the rear position. </h3></li><li><h3>Check whether the queue is full – [i.e., the rear end is in just before the front end in a circular manner].</h3></li><li>• <h3>• If it is full then display Queue is full. </h3></li><li><h3>• </h3><h3>• If the queue is not full then,  insert an element at the end of the queue.</h3></li><li>• <h3>• </h3><strong><h3>deQueue()</h3></strong><h3> This function is used to delete an element from the circular queue. In a circular queue, the element is always deleted from the front position. </h3></li><li><h3>Check whether the queue is Empty.</h3></li><li>• <h3>• If it is empty then display Queue is empty.</h3></li><li><h3>• </h3><h3>• If the queue is not empty, then get the last element and remove it from the queue.</h3></li></ul></p><p></p><p><img src="images/16-9.png" alt="images/16-9.png" /></p><p></p><p></p><p></p><p><strong><h2>Implement Circular Queue using Array:</h2></strong></p><p><ul><li>• <strong>•</strong> <h3>Initialize an array queue of size </h3><strong><h3>n</h3></strong><h3>, where n is the maximum number of elements that the queue can hold.</h3></li><li>• <strong>•</strong> <h3>Initialize two variables front and rear to -1.</h3></li><li>• <strong>•</strong> <strong><h3>Enqueue:</h3></strong><h3> To enqueue an element </h3><strong><h3>x</h3></strong><h3> into the queue, do the following:• Increment rear by 1.</h3></li><li><h3>• </h3><h3>• If </h3><strong><h3>rear</h3></strong><h3> is equal to n, set </h3><strong><h3>rear</h3></strong><h3> to 0.</h3></li><li>• <strong><h3>•</h3></strong><h3> If </h3><strong><h3>front</h3></strong><h3> is -1, set </h3><strong><h3>front</h3></strong><h3> to 0.</h3></li><li>• <strong><h3>•</h3></strong><h3> Set queue[rear] to x.</h3></li></ul></p><p></p><p><ul><li>• <strong><h3>•</h3></strong><h3> </h3><strong><h3>Dequeue:</h3></strong><h3> To dequeue an element from the queue, do the following:◇ Check if the queue is empty by checking if </h3><strong><h3>front</h3></strong><h3> is -1. </h3></li><li><h3>• </h3><h3>• If it is, return an error message indicating that the queue is empty.</h3> <h3>Set </h3><strong><h3>x</h3></strong><h3> to queue[front].</h3></li><li>• <strong><span style="indent:1;">• </span></strong><h3>If </h3><strong><h3>front</h3></strong><h3> is equal to </h3><strong><h3>rear</h3></strong><h3>, set </h3><strong><h3>front</h3></strong><h3> and </h3><strong><h3>rear</h3></strong><h3> to -1.</h3></li><li>• <strong><h3>•</h3></strong><h3> Otherwise, increment </h3><strong><h3>front</h3></strong><h3> by 1 and if </h3><strong><h3>front</h3></strong><h3> is equal to n, set </h3><strong><h3>front</h3></strong><h3> to 0.</h3></li><li>• <strong><h3>•</h3></strong><h3> Return x.</h3></li></ul></p><p></p><p></p><p><strong><h2>Complexity Analysis of Circular Queue Operations:</h2></strong><ul><li>• <h3>• </h3><strong><h3>Time Complexity:</h3></strong><h3> </h3></li><li><h3> Enqueue: O(1) because no loop is involved for a single enqueue.</h3></li><li><h3> Dequeue: O(1) because no loop is involved for one dequeue operation.</h3></li></ul></p><p></p><p><ul><li>• <h2>• </h2><strong><h2>Auxiliary Space:</h2></strong><h2> O(N) as the queue is of size N.</h2></li></ul></p><p></p><p></p><p><strong><h2>Applications of Circular Queue:</h2></strong><ul><li><h3> </h3><strong><h3>Memory Management:</h3></strong><h3> The unused memory locations in the case of ordinary queues can be utilized in circular queues.</h3></li><li><h3> </h3><strong><h3>Traffic system:</h3></strong><h3> In computer controlled traffic system, circular queues are used to switch on the traffic lights one by one repeatedly as per the time set.</h3></li><li> <strong><h3>CPU Scheduling:</h3></strong><h3> Operating systems often maintain a queue of processes that are ready to execute or that are waiting for a particular event to occur.</h3></li></ul></p><p><h3> </h3></p><p></p><p></p><p><strong><h2>This queue is primarily used in the following cases:</h2></strong></p><p><ol><li>1. <h3>1. </h3><strong><h3>Memory Management:</h3></strong><h3> The unused memory locations in the case of ordinary queues can be utilized in circular queues.</h3></li><li>2. <h3>2. </h3><strong><h3>Traffic system:</h3></strong><h3> In a computer-controlled traffic system, circular queues are used to switch on the traffic lights one by one repeatedly as per the time set.</h3></li><li>3. <h3>3. </h3><strong><h3>CPU Scheduling:</h3></strong><h3> Operating systems often maintain a queue of processes that are ready to execute or that are waiting for a particular event to occur.</h3></li></ol></p><p></p><p><h3>The time complexity for the circular Queue is O(1).</h3></p><p></p><p><strong><h2> </h2></strong><strong><h2>Output restricted Queue</h2></strong><strong><span style="color:#7b6e00;">:</span></strong><span style="color:#7b6e00;"></span></p><p><span style="color:#7b6e00;"></span><span style="color:#7b6e00;"></span></p><p><span style="color:#7b6e00;"></span><h3>In this type of Queue, the input can be taken from both sides(rear and front) and the deletion of the element can be done from only one side(front).  This queue is used in the case where the inputs have some priority order to be executed and the input can be placed even in the first place so that it is executed first. </h3><span style="color:#26a269;"></span></p><p><span style="color:#26a269;"></span></p><p><img src="images/16-10.png" alt="images/16-10.png" /></p><p></p><p></p><p><strong><h3> Input restricted Queue:</h3></strong><h3> In this type of Queue, the input can be taken from one side only(rear) and deletion of elements can be done from both sides(front and rear). This kind of Queue does not follow FIFO(first in first out).  This queue is used in cases where the consumption of the data needs to be in FIFO order but if there is a need to remove the recently inserted data for some reason and one such case can be irrelevant data, performance issue, etc. </h3></p><p></p><p><img src="images/16-11.png" alt="images/16-11.png" /></p><p></p><p> <strong><h2>Double ended Queue</h2></strong><strong><h2>:</h2></strong><h3></h3></p><p><h3></h3><h3></h3></p><p><h3> Double Ended Queue is also a Queue data structure in which the insertion and deletion operations are performed at both the ends (front and rear). That means, we can insert at both front and rear positions and can delete from both front and rear positions.  Since Deque supports both stack and queue operations, it can be used as both. The Deque data structure supports clockwise and anticlockwise rotations in O(1) time which can be useful in certain applications. Also, the problems where elements need to be removed and or added both ends can be efficiently solved using Deque.</h3></p><p></p><p><img src="images/16-12.png" alt="images/16-12.png" /></p><p></p><p><strong><h2> Priority Queue</h2></strong><strong><h2>:</h2></strong><span style="color:#7e0000;"></span></p><p><span style="color:#7e0000;"></span><span style="color:#7e0000;"></span></p><p><span style="color:#7e0000;"></span><h3>A priority queue is a special type of queue in which each element is associated with a priority and is served according to its priority. </h3><span style="color:#7e0000;"></span></p><p><span style="color:#7e0000;"></span><span style="color:#7e0000;"></span></p><p><span style="color:#7e0000;"></span><strong><h2>Properties of Priority Queue</h2></strong><span style="color:#7e0000;"></span></p><p><span style="color:#7e0000;"></span><em><h3>So, a priority Queue is an extension of the </h3></em>queue <em><h3>with the following properties.</h3></em><em><strong><h3> </h3></strong></em><ul><li><h3>Every item has a priority associated with it.</h3></li><li><h3>An element with high priority is dequeued before an element with low priority.</h3></li><li><h3>If two elements have the same priority, they are served according to their order in the queue.</h3></li></ul><span style="color:#7e0000;"></span></p><p><span style="color:#7e0000;"></span><span style="color:#7e0000;"></span></p><p><span style="color:#7e0000;"></span><h3>In the below priority queue, an element with a maximum ASCII value will have the highest priority. The elements with higher priority are served first. </h3><span style="color:#7e0000;"></span></p><p><span style="color:#7e0000;"></span><img src="images/16-13.png" alt="images/16-13.png" /></p><p></p><p><strong><h2>How is Priority assigned to the elements in a Priority Queue?</h2></strong></p><p><h3>In a priority queue, generally, the value of an element is considered for assigning the priority. </h3></p><p><h3>For example, the element with the highest value is assigned the highest priority and the element with the lowest value is assigned the lowest priority. The reverse case can also be used i.e., the element with the lowest value can be assigned the highest priority. Also, the priority can be assigned according to our needs. </h3></p><p></p><p><strong><h2>Operations of a Priority Queue:</h2></strong></p><p><h3>A typical priority queue supports the following operations:</h3></p><p><ol><li>1) <strong><h3>1) Insertion in a Priority Queue</h3></strong></li></ol></p><p><h3>When a new element is inserted in a priority queue, it moves to the empty slot from top to bottom and left to right. However, if the element is not in the correct place then it will be compared with the parent node. If the element is not in the correct order, the elements are swapped. The swapping process continues until all the elements are placed in the correct position.</h3></p><p><ol><li>2) <strong><h3>2) Deletion in a Priority Queue </h3></strong><h3> </h3></li></ol></p><p><h3>As you know that in a max heap, the maximum element is the root node. And it will remove the element which has maximum priority first. Thus, you remove the root node from the queue. This removal creates an empty slot, which will be further filled with new insertion. Then, it compares the newly inserted element with all the elements inside the queue to maintain the heap invariant.</h3></p><p><ol><li>3) <strong><h3>3) Peek in a Priority Queue</h3></strong></li></ol></p><p><h3>This operation helps to return the maximum element from Max Heap or the minimum element from Min Heap without deleting the node from the priority queue.</h3></p><p></p><p><h2>Types of Priority Queue:</h2></p><p><ol><li>1) <strong><h3>1) Ascending Order Priority Queue</h3></strong></li></ol></p><p><h3>As the name suggests, in ascending order priority queue, the element with a lower priority value is given a higher priority in the priority list. For example, if we have the following elements in a priority queue arranged in ascending order like 4,6,8,9,10. Here, 4 is the smallest number, therefore, it will get the highest priority in a priority queue and so when we dequeue from this type of priority queue, 4 will remove from the queue and dequeue returns 4.</h3></p><p><ol><li>2) <strong><h3>2) Descending order Priority Queue </h3></strong></li></ol></p><p><h3>The root node is the maximum element in a max heap, as you may know. It will also remove the element with the highest priority first. As a result, the root node is removed from the queue. This deletion leaves an empty space, which will be filled with fresh insertions in the future. The heap invariant is then maintained by comparing the newly inserted element to all other entries in the queue.</h3></p><p><img src="images/16-14.png" alt="images/16-14.png" /></p><p></p><p><ol><li>1) <strong><h2>1) Implement Priority Queue Using Array:</h2></strong><em><h2> </h2></em></li></ol></p><p><h3>A simple implementation is to use an array of the following structure. </h3></p><p><h3>struct item {</h3><h3></h3></p><p><h3>        int item;</h3><h3></h3></p><p><h3>        int priority;</h3><h3></h3></p><p><h3>}</h3></p><p><ul><li>• <h3>• </h3><strong><h3>enqueue():</h3></strong><h3> This function is used to insert new data into the queue.</h3></li><li>• <h3>• </h3><strong><h3>dequeue():</h3></strong><h3> This function removes the element with the highest priority from the queue.</h3></li><li>• <h3>• </h3><strong><h3>peek()/top():</h3></strong><h3> This function is used to get the highest priority element in the queue without removing it from the queue</h3></p><p></li></ul><table class="table"><tr><th>Arrays</th><th>enqueue()</th><th>dequeue()</th><th>peek()</th></tr><tr><td>Time Complexity</td><td>O(1)</td><td>O(n)</td><td>O(n)</td></tr></table></p><p></p><p><ol><li>2) <strong><h3>2) Implement Priority Queue Using Linked List: </h3></strong></li></ol></p><p><h3>In a LinkedList implementation, the entries are sorted in descending order based on their priority. The highest priority element is always added to the front of the priority queue, which is formed using linked lists. The functions like </h3><strong><h3>push()</h3></strong><h3>, </h3><strong><h3>pop()</h3></strong><h3>, and</h3><strong><h3> peek()</h3></strong><h3> are used to implement a priority queue using a linked list and are explained as follows:</h3><ul><li><strong>push(): </strong><h3>This function is used to insert new data into the queue.</h3></li><li><strong>pop(): </strong><h3>This function removes the element with the highest priority from the queue.</h3></li><li><strong>peek() / top(): </strong><h3>This function is used to get the highest priority element in the queue without removing it from the queue.</h3></li></ul></p><p></p><p><table class="table"><tr><th>Linked List</th><th>push()</th><th>pop()</th><th>peek()</th></tr><tr><td>Time Complexity</td><td>O(n)</td><td>O(1)</td><td>O(1)</td></tr></table></p><p></p><p></p></div>
</body>
</html>