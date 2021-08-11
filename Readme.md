<div align="center" float=""left>

  <p float="left">
  <img height="60" src="https://img.icons8.com/color/344/python.png" />
  <img height="60" src="https://img.icons8.com/color/344/javascript.png" /> 
  </p>
  <h1>50 Awesome Leetcode In Python + Javascript</h1>
  
 ---
  <span> This Repository contains all the notes and the code executions with detailed explanations for the codes and the theoretical implementations. In future I'll hook in the codes along with the explanations in my <a href="https://www.instagram.com/jayasoruban1112/">Instagram</a> **stories**, which I'll also post here.
	  
LeetCode is essentially a huge repository of real interview questions asked by the most popular tech companies ( Google, Amazon, Facebook, Microsoft, and more ).
The problem with LeetCode is also its advantage, IT'S HUGE, so huge in fact that interviewers from the most popular companies often directly ask questions they find on LeetCode, So it's hard to navigate through the huge amount of problems to find those that really matter, this is what this repo is for.

From Basic to Advanced Refresh your Python implementations of Leetcodes with theoretical addons. I have added the answers in the **collapsed sections** below the questions , simply click on them to expand. **Javascript Implementations are also hooked in!! Do check it**. It'll trigger you Cognizance and makes you a better learner. Good luck! ❤️ </span>

Feel free to reach out to me! (❁´◡`❁)🤗<br/>
  <a href="https://www.instagram.com/jayasoruban1112/">Instagram</a> || 
  <a href="https://twitter.com/jayasoruban">Twitter</a> || 
  <a href="https://in.linkedin.com/in/jayasoruban-js-67b35b1bb">LinkedIn</a> ||
  <a href="#">Website</a> ||

</div>

| Feel free to fork and use it for your coding practices! 😃  I would _really_ appreciate a reference to this repo, These notes and code snippets make one a better learner I believe 💪🏼 . Lets be a cohort of Awesome Coders and share the immortal knowledge forever🌏 Thank you and have fun!   |
|---|

<h1>DataStructures And Algorithms Used In The Codes</h1>
<ul>
	<li>Arrays and Strings interview questions.</li>
	<li>Searching interview questions and algorithms.</li>
	<li>Dynamic Programming interview questions.</li>
	<li>Backtracking interview questions (  With step by step visualization ).</li>
	<li>Trees and Graphs interview questions and algorithms.</li>
	<li>Data structures Like Stacks, Queues, Maps, Linked Lists, and more</li>
</ul>

---
<h1>Section 1</h1>
<h2> Big O Notation</h2>
<p>Algorithm analysis refers to the analysis of the complexity of different algorithms and finding the most efficient algorithm to solve the problem at hand. Big-O Notation is a statistical measure, used to describe the complexity of the algorithm.</p>

```
def fact(n):
  product = 1
  for i in range(n):
    product = product * (i+1)
    return product
print (fact(5))
```

```
def fact2(n):
  if n == 0:
    return 1
  else:
    return n * fact2(n-1)
print (fact2(5))
```
<ul>
  <li>If we use %%timeit the the first Algorithm which uses <strong>looping</strong> takes 9 microseconds and second algorithm using <strong>recursion</strong> takes 15 microsecond</li>
  <li>The execution time shows that the first algorithm is faster compared to the second algorithm involving recursion. This example shows the importance of algorithm analysis. In the case of large inputs, the performance difference can become more significant.</li>
  <li>However, execution time is not a good metric to measure the complexity of an algorithm since it depends upon the hardware. A more objective complexity analysis metrics for the algorithms is needed. <b>This is where Big O notation comes to play</b>.</li>
</ul>

<h4>Algorithm Analysis with Big-O Notation</h4>
  
  ```
  **Big O Notations**
  1) Constant      O(c)
  2) Linear        O(N)
  3) Quadratic     O(N^2)
  3) Cubic         O(N^3)
  4) Exponential   O(2^N)
  5) Logarithmic   O(log(N))
  6) Log Linear    O(Nlog(N))
  
  ```
  
<h5>1) Constant Complexity</h5>
<p>The complexity of an algorithm is said to be constant if the steps required to complete the execution of an algorithm remain constant, irrespective of the number of inputs. The constant complexity is denoted by O(c) where c can be any constant number.</p>


```
## Python
def constant_algo(items):
    result = items[0] * items[0]
    print ()

constant_algo([4, 5, 6, 8])
```
```
/*C*/
void printFirstElementOfArray(int arr[])
{
    printf("First element of array = %d",arr[0]);
}
```
![image](https://user-images.githubusercontent.com/79846829/128961165-d1204046-4458-4c82-9b9c-3546e6adc8ea.png)

<p>irrespective of the input size, or the number of items in the input list items, the algorithm performs only constant steps</p>


<h5>2) Linear Complexity</h5>
<p>The complexity of an algorithm is said to be linear if the steps required to complete the execution of an algorithm increase or decrease linearly with the number of inputs. Linear complexity is denoted by O(n).
</p>


```
## Python
def linear_algo(items):
    for item in items:
        print(item)

linear_algo([4, 5, 6, 8])
```
```
/*C*/
void printAllElementOfArray(int arr[], int size)
{
    for (int i = 0; i < size; i++)
    {
        printf("%d\n", arr[i]);
    }
}
```
![image](https://user-images.githubusercontent.com/79846829/128961488-646b43cb-6ecf-424d-a36d-afdc97269ed0.png)

<p>The complexity of the linear_algo function is linear in the above example since the number of iterations of the for-loop will be equal to the size of the input items array.</p>



<h5>3) Quadratic Complexity</h5>
<p>The complexity of an algorithm is said to be quadratic when the steps required to execute an algorithm are a quadratic function of the number of items in the input. Quadratic complexity is denoted as O(n^2)
</p>


```
## Python
def quadratic_algo(items):
    for item in items:
        for item2 in items:
            print(item, ' ' ,item)

quadratic_algo([4, 5, 6, 8])
```
```
/*C*/
void printAllPossibleOrderedPairs(int arr[], int size)
{
    for (int i = 0; i < size; i++)
    {
        for (int j = 0; j < size; j++)
        {
            printf("%d = %d\n", arr[i], arr[j]);
        }
     }
}
```
![image](https://user-images.githubusercontent.com/79846829/128961672-8949da42-d385-43a6-8c58-e2b5cea28814.png)

<p>In the script above, you can see that we have an outer loop that iterates through all the items in the input list and then a nested inner loop, which again iterates through all the items in the input list. The total number of steps performed is n * n, where n is the number of items in the input array.</p>

<h5>Drop The Constants</h5>
<p>When you're calculating the big O complexity of something, you just throw out the constants. Like:</p>

```
void printAllItemsTwice(int arr[], int size)
{
    for (int i = 0; i < size; i++)
    {
        printf("%d\n", arr[i]);
    }
	
    for (int i = 0; i < size; i++)
    {
        printf("%d\n", arr[i]);
    }
}
```
<p>This is O(2n), which we just call O(n).</p>

```
void printFirstItemThenFirstHalfThenSayHi100Times(int arr[], int size)
{
    printf("First element of array = %d\n",arr[0]);
	
    for (int i = 0; i < size/2; i++)
    {
        printf("%d\n", arr[i]);
    }

    for (int i = 0; i < 100; i++)
    {
        printf("Hi\n");
    }
}
```
<p>This is O(1 + n/2 + 100), which we just call O(n).</p>

```
void printAllNumbersThenAllPairSums(int arr[], int size)
{
    for (int i = 0; i < size; i++)
    {
        printf("%d\n", arr[i]);
    }

    for (int i = 0; i < size; i++)
    {
        for (int j = 0; j < size; j++)
        {
            printf("%d\n", arr[i] + arr[j]);
        }
    }
}
```
<p>Here our runtime is O(n + n2), which we just call O(n2).</p>











