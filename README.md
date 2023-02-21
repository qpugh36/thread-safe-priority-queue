# thread-safe-priority-queue
In this code, the PriorityQueue class is implemented using the singleton design pattern to ensure that there is only one instance of the priority queue that is shared across threads. The priority queue itself is implemented using a binary heap data structure, which provides efficient access to the highest-priority item.

To ensure thread safety, the push and pop methods of the priority queue are synchronized using a mutex and condition variable. The push method adds an item to the queue and notifies any waiting threads that an item has been added. The pop method waits for an item to be added to the queue, then removes and returns the highest-priority item.

To demonstrate the functionality of the priority queue, the code includes two thread functions, producer and consumer, which add and remove items from the queue, respectively. These functions are executed in separate threads using the std::thread class.

Finally, the code includes a unit test using the Google Test framework. The test creates a producer thread and a consumer thread, which add and remove items from the queue, respectively. The test asserts that the items are removed in the correct order using the EXPECT_EQ macro.

Overall, this code demonstrates the use of C++11 or newer features to implement a thread-safe priority queue using the singleton design pattern
