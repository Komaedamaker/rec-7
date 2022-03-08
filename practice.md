# CSCI 2270 – Midterm 1, Part II: Practice Problem



You are given a singly linked list class. This class has two head nodes, such that it can
contain two separate linked lists. Your task is to complete the appropriate function that,
on satisfying a given condition, takes the linked list pointed to by the first head pointer,
and splits it into two Linked Lists, such that the second head pointer becomes the head
pointer of the second list.
 
## Starer Code and Submission:
You must complete the following two functions:

1. `int split(string searchKey){...}` (35 points)
2. `~SLL(){...}` (5 points)

The starter code is included in the `code_1` directory. You are only allowed to make changes to the specified functions in `LinkedList.cpp`. Do not change `LinkedList.hpp`. You can do whatever you want in `app_1/main_1.cpp`, but it will not affect your grade. 

Note that you are not guaranteed to receive full points just by passing the given test
cases. Your algorithm also has to be correct and not introduce any memory leaks.

### Specifications:

1. The `split` function takes in a `searchKey` string value.

2. If `searchKey` exists, the linked list gets split into two separate lists:
+ The node matching searchKey becomes the headTwo
+ If the `searchKey` is found at `headOne`, then the first list becomes an
empty list (`headOne` gets set to `nullptr`), and `headTwo` becomes the
head of the list
+ Function returns integer value of 0

3. If searchKey does not exist in the linked list, the function does nothing and
returns an integer value of 1.

4. The constructor is defined and initializes both the head nodes to 'nullptr'. It is also overloaded such that if it is called with the string “demo” it will generate a single linked list with the strings “che”,”the”, “fluffy”, “cat”, with `headOne` pointing to the node containing “che”, and `headTwo` pointing to `nullptr`. See example below.

7. Complete the destructor definition such that all of the dynamic memory is properly deallocated.


### Example 
Let `li` be an object of the `LinkedList` class. If `li` has the following initial configuration:

<img src="./images/demo.png" width="600">

After a call to `int result = li.split("fluffy");` it should look like:

<img src="./images/result.png" width="600">

and the value in `result` should be 0;

##  Instructions - Getting and submitting code

 1. Open up your Linux terminal, navigate to the build directory of this assignment (e.g. `cd build`).
 2. Run the `cmake ..` command.
 3. Run the `make` command.
 4. If there are no compilation errors, two executables will be generated within the build directory: `run_app_1` and `run_tests`.
 5. If you would like to run your program including your app implementation in the `main` function, execute `run_app_1` from the terminal by typing `./run_app_1`.
 6. To run the grading tests, execute `run_tests` from the terminal by typing `./run_tests`. 
 7. Your submission will be the code you commit and push by the exam end time. (Note: you do NOT need to paste your link back into Canvas.) 
 
### Reminder - this is how you submit in GitHub:
 * Stage:
     ```console
     $ git add ../code_1/LinkedList.cpp
     ```
 
 * Commit the changes to our local repository:
     ```console
     $ git commit -m 'this is my commit'
     ```
 
* Push to GitHub: 
     ```console
     $ git push
    ```