Deepak works for Indian Railways and is analyzing train stop patterns. 
The network has `n` stations numbered 1 to `n`. Each train has a starting station `s`,
ending station `e`, and step value `k` — meaning it stops at stations `s`, `s + k`, `s + 2k`, ... up to `e` (inclusive).

For the given trains, determine:  
- The stop sequence for each train (printed on separate lines)  
- The total number of stops across all trains  
- The smallest station number where all trains stop (or `-1` if no such station exists)

---

### **Input Format**

First line: integer `t` (1 ≤ t ≤ 10) — number of trains  
Second line: integer `n` (5 ≤ n ≤ 50) — total number of stations in the network  
For each train, three lines:  
- `s` (starting station, 1 ≤ s ≤ n)  
- `e` (ending station, s ≤ e ≤ n)  
- `k` (step value, 1 ≤ k ≤ n)

---

### **Output Format**

For each train: print a line containing space-separated station numbers where it stops (in increasing order).  
After all train sequences, print a blank line, then two lines:  
- Total number of stops across all trains  
- Smallest station where all trains stop, or `-1` if none exists
