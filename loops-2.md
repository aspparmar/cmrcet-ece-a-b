Rajesh manages a large warehouse for an e-commerce company in Bengaluru. 
Every week, he receives a shipment manifest containing product quantities across multiple categories. 
To quickly assess the shipment, Rajesh needs a program that calculates the cumulative running total 
of items as he scans through each category.

Given `n` integers representing the quantity of items in each category (entered one per line),
help Rajesh generate a running total sequence. The running total at any position is the sum of all 
quantities from the first category up to and including the current category.

Additionally, Rajesh wants to know the position (1-indexed) at which the cumulative total first exceeds
or equals a given threshold `t`. If the threshold is never reached, report `-1`.

---

### **Input Format**

The first line contains an integer `n` (1 ≤ n ≤ 100), representing the number of categories.  
The second line contains an integer `t` (1 ≤ t ≤ 100000), representing the threshold value.  
The next `n` lines each contain a single integer representing the quantity of items in that category. Each quantity is between 1 and 1000 (inclusive).

---

### **Output Format**

Print `n` lines where each line contains the cumulative total up to that category.  
The last line should contain a single integer representing the 1-indexed position where the cumulative total first meets or exceeds the threshold `t`, or `-1` if it never does.
