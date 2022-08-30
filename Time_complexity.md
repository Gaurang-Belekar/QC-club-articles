# Time Complexity
### **Introduction:**
In computer science, time complexity is the amout of time taken for an algorithm to run. It does not consider the actul time that is taken to execute a code, but the number of times each statement executes. An algorithm’s running time varies with the variation in the input size. As a result of this, we usually consider the worst-case time complexity for an algorithm. Worst-case time complexity is the maximum time taken by an algorithm to run for a specified number of inputs. Time complexity is usually expressed as a function of the input size. Since this function is difficult to compute, we focus on its behaviour when the input size increases. In this article, we will look into how this complexity is expressed and a few complexity classes. We will also peek into one of the most difficult problems that is yet unsolved.
<br><br>
### **Big O Notation:**
Big O Notation is used to tell the complexity and compare between any two algorithms by considering a number of operations taken by it for a given data set to the program. The time taken and the space requirements change according to the input size growth. While many other factors also affect the complexity, Big O considers all other except numbers of operations of an algorithm to be constant. 
<br><br>
***NOTE:*** Big O doesn’t tell you about the speed of an algorithm. It is denoted by O(n), where n is the number of operations.
<br><br>
### **Why?**
Big O Notation helps programmers to measure the scalability of algorithms and to gauge the efficiency of the program they write. It finds the limiting behavior of a function when the argument tends towards a particular value or infinity. The letter ‘O’ is used because the growth rate of a function is referred to as the “Order of the function”.
<br><br>
### **Anology:**
Say you want to find your favorite superstar’s phone number in the telephone directory then you write a simple search algorithm to do this. Then it takes O(n) times to run i.e, every single record we need to check. But, say if it is found in the 1st try itself then the complexity is O(1).
<br><br>
### **examples:**
* Binary Search                                                                                O(n)
* Binary Search                                                                                O(logn)
* Quick Sort                                                                                     O(n*logn)
* Selection Sort                                                                               O(n^2)

It is one of the family of asymptotic notation (asymptotic analysis – other than the “input” all other factors are considered constant, computing the running time of any operation in mathematical units of computation.). They are called Bachmann- landau notations as they were the prominent Number Theorists who invented these notations for asymptotic analysis back in those days. But Donald Knuth is the scientist who is prominent in popularizing it in the field of computer science. 
 
The best part of Big O Notation is that it sees the worst-case scenario and this helps to improve the efficiency of an algorithm as it says that the upper bound on the growth rate of a function is the best one and most generally used in finding complexity. 
<br><br>
### **P(Polynomial Time):**
When an algorithm with input size n, runs in time O(nk) where k is a positive number, then the algorithm is said to be running in polynomial time. In other words, when the operational complexity of an algorithm with n inputs is proportional to nc, where c is some constant, then the algorithm is running in polynomial time. Polynomial-time algorithms are also known to be efficient and fast. Selection sort is an example of a polynomial time algorithm as the running time for this algorithm for n inputs is O(n2). Basic operations like addition, subtraction, multiplication, division, etc. can also be done in polynomial time.
<br><br>
### **NP(Nondeterministic Polynomial Time):**
NP complete problem type lies at the intersection of NP and NP hard. You can convert a solver for an NP-Hard problem type into a solver of any NP problem using polynomial resources such as time or memory. So solving any NP Hard problem can take you to solving any NP type problem, which would mean that you can solve any P type problem. This also implies that if you find a polynomial time solution, you can also find P=NP. This has not happened yet and is not expected to happen. 
<br><br>
### **P vs NP:**
It is one of the unsolved problems in theoretical computer science that the Clay Mathematics Institute will give a million dollars to one when proved or disproved. The problem soughts to find the solution to whether P is equivalent to NP or not. In layman's terms, it tries to find whether every problem whose answer can be verified in polynomial time can also be solved in polynomial time. 

P is a set of relatively easy problems while NP is a set of extremely difficult problems. If P = NP, it would suggest that problems which are extremely difficult have relatively easy solutions, however it includes several complexities. This leads to the fact that a vast majority of NP problems which seem to take up exponential time are known as NP-complete, meaning that the polynomial time solution for one problem can be used for all others. Thus, P is probably not equal to NP, but this problem is open to other solutions.
<br><br>
### **BQP:**
BQP, in computational complexity theory, stands for "Bounded error, Quantum, Polynomial time". It denotes the class of problems solvable by a quantum computer in polynomial time, with an error probability of at most 1/4 for all instances. In other words, there is an algorithm for a quantum computer that is guaranteed to run in polynomial time. On any given run of the algorithm, it has a probability of at most 1/4 that it will give the wrong answer. That is true, whether the answer is YES or NO. 
 
The choice of 1/4 in the definition is arbitrary. Changing the constant to any real number k such that 0 < k < 1/2 does not change the set BQP. The idea is that there is a small probability of error, but running the algorithm produces an exponentially-small chance several times that the majority of the runs are wrong. 
 
The number of qubits in the computer is allowed to be a function of the instance size. For example, algorithms are known for factoring an n-bit integer using just over 2n qubits. Quantum computers have gained widespread interest because some problems of practical interest are known to be in BQP, but suspected to be outside P. Currently, only three such problems are known: 
* Integer factorization(see Shor's algorithm)
* Discrete logarithm
* Simulation of quantum systems (see universal quantum computer) 

This class is defined for a quantum computer. The corresponding class for an ordinary Turing machine plus a source of randomness is BPP. 
 
BQP contains P and BPP and is contained in PP and PSPACE. In fact, BQP is low for PP, meaning that a PP machine achieves no benefit from being able to solve BQP problems instantly, an indication of the vast difference in power between these similar classes. 
<br><br>
### **BQP,P and NP:**
First of all, we know that P is a subset of BQP since every classical circuit can be simulated by a quantum circuit. It is conjectured that BQP solves hard problems outside of P, specifically problems in NP. The claim is unspecified because we don't know if P=NP, so we don't know if those problems are actually in P.

![PP complexity](https://upload.wikimedia.org/wikipedia/commons/thumb/9/9e/Randomised_Complexity_Classes_2.svg/280px-Randomised_Complexity_Classes_2.svg.png)

Here RP refers to randomized Polynomial Time 

Here ZP refers to zero-error probabilistic polynomial time 
<br><br>
### **BQP vs BPP:**
In computational complexity theory, a branch of computer science, bounded-error quantum polynomial time (BQP) is the class of decision problems solvable by a quantum computer in polynomial time, with an error probability of at most 1/3 for all instances. It is the quantum analogue to the complexity class BPP. 
 
Bounded-error probabilistic polynomial time (BPP) is the group of decision problems solvable by a probabilistic Turing machine in polynomial time with an error probability bounded away from 1/3 for every instance. BPP is one of the largest practical classes of problems, meaning most problems of interest in BPP have efficient probabilistic algorithms that can be run quickly on real modern machines. BPP also contains P, the class of problems solvable in polynomial time with a deterministic machine, since a deterministic machine is a special case of a probabilistic machine. 

![BQP vs BPP](https://upload.wikimedia.org/wikipedia/commons/thumb/1/1d/BQP_complexity_class_diagram.svg/440px-BQP_complexity_class_diagram.svg.png)

Better results are known for class BQP with rspect to BPP and other probabilistic classes. 
Have a look at the diagram.

![BPP complexity](https://i.ytimg.com/vi/0VnlNJj8Ljk/maxresdefault.jpg)
<br><br>
## **Conclusion:**
We have tried to give a glimpse into some complexity classes and the famous unsolvable problem of P vs NP. Hence we see that the problems still remain difficult to solve with classical computers. This problem, though unsolvable, is expected to be solved with the help of a quantum computer. Also, the concept of time complexity is a very important one for algorithms and helps us choose the best time specific algorithms for a certain task.

### **References:**
https://en.wikipedia.org/wiki/File:Randomized_Complexity_Classes.svg


                                                                            ~Quantum Computing Club
                                                                                      IIIT Dharward
### **Authors**
Shreya Talekar

Shriya Patare

S Karan Raj

Sujith Makam 

N Yaswanth Kumar
