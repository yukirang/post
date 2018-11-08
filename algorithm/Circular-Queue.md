We know that the queue is a data structure based on <a href="https://en.wikipedia.org/wiki/FIFO_(computing_and_electronics)">FIFO </a>(First In First Out) principle. Adding an element in a queue is only allowed at the rear of the queue. It is easy to notice that when the queue is unable to hold more element at back, even if there are spots left in front of the queue, no more can be crammed in.

Imagine we have released a lot of spaces at the head, is there any way to reuse these spaces? The answer is exactly the Circular Queue. In a circular queue, the rear is connected to the head, forming a circular structure. The front and rear pointers move clockwise with "enqueue" and "dequeue" operations.

[caption id="" align="aligncenter" width="289"]<img class="" src="https://cdncontribute.geeksforgeeks.org/wp-content/uploads/Circular-queue.png" width="289" height="300" /> Circular Queue[1][/caption]Now let's grab a sense of how to implement the Circular Queue:
<pre lang="javascript" line="0">//Initialization. Set the size of the queue to be k.
var MyCircularQueue = function(k) {
    this.queue = new Array(k);
    this.head = 0;
    this.tail = 0;
    this.size = k-1;
    this.count = 0;
};

//Insert an element into the circular queue. 
MyCircularQueue.prototype.enQueue = function(value) {
    if(this.count &lt; this.size+1){
        if(this.count === 0){
            ;
        }
        else if(this.tail &lt; this.size){
            this.tail++;
        }else{
            this.tail = 0;
        }
        this.queue[this.tail] = value;
        this.count++;
        return true;
    }else{
        return false;
    }
};



// Get the front item from the queue.
MyCircularQueue.prototype.Front = function() { if(this.count &gt; 0)
        return this.queue[this.head];
    else
        return -1;
};


//Get the last item from the queue.
MyCircularQueue.prototype.Rear = function() {
    if(this.queue[this.tail] != undefined)
        return this.queue[this.tail];
    else
        return -1;
};

//Checks whether the circular queue is empty or not.
MyCircularQueue.prototype.isEmpty = function() {
   if(this.count === 0){
       return true;
   }else{
       return false;
   }
};

//Checks whether the circular queue is full or not.
MyCircularQueue.prototype.isFull = function() {
    if(this.count === this.size+1)
        return true;
    else
        return false;
};
</pre>
References

[1]"Circular Queue | Set 1 (Introduction and Array Implementation) - GeeksforGeeks", <i>GeeksforGeeks</i>, 2018. [Online]. Available: https://www.geeksforgeeks.org/circular-queue-set-1-introduction-array-implementation/. [Accessed: 08- Nov- 2018].

&nbsp;