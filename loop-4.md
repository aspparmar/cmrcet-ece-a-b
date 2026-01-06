Ananya is a quantitative analyst at a stock brokerage firm in Mumbai. She analyzes stock price movements over multiple days, where each day is divided into `w` trading windows.

For each day, she needs to:  
- Calculate the sum of all window prices  
- Determine if the day was `"BULLISH"` (last price > first price), `"BEARISH"` (last price < first price), or `"NEUTRAL"` (equal)

After all days, she needs to report:  
- The total sum of all prices across all days  
- The count of `"BULLISH"` days  
- The longest streak of consecutive `"BULLISH"` days (note: `"NEUTRAL"` days do not break the streak but do not extend it either)  
- The first day number (1-indexed) where any price was less than its previous window price within that day. Report `-1` if no such drop occurred.

---

### **Input Format**

The first line contains an integer `days` (1 ≤ days ≤ 20), representing the number of trading days.  
The second line contains an integer `w` (2 ≤ w ≤ 10), representing the number of trading windows per day.  
The next `days × w` lines each contain a single integer (1 to 10000) representing the stock price for each window, given in order.

---

### **Output Format**

For each day, print the daily sum followed by a space and the trend (`"BULLISH"`, `"BEARISH"`, or `"NEUTRAL"`).  
After all days, print a blank line, then four lines containing:  
- Total sum of all prices  
- Count of `"BULLISH"` days  
- Longest streak of consecutive `"BULLISH"` days  
- First day number where an intra-day price drop occurred, or `-1` if none

### example : 
 **input** :
`
3
4
100
110
120
130
200
190
185
180
150
155
160
170
`
  ** output**:
`
460 BULLISH
755 BEARISH
635 BULLISH

1850
2
1
2
`
