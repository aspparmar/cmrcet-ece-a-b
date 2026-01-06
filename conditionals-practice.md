"QuickBite" is a food delivery app that has a complex discount system to reward customers. 
The discount engine applies multiple rules based on the order details, and the rules must be
checked in a specific order. Once a discount is applied, no other discount can be added (discounts do not stack).

The discount rules, checked in this exact order, are:

1. **First-Time User Bonus**:  
   If the customer is a first-time user (`1` for yes, `0` for no) AND the order value is ₹200 or more, apply a **20% discount**.  
   → Discount type: `"First Order Bonus"`

2. **Premium Member Discount** (only if Rule 1 does **not** apply):  
   If the customer is a premium member (`1` for yes, `0` for no):  
   - Order value ₹500 or more → **15% discount** (`"Premium Elite"`)  
   - Order value ₹250 to ₹499 → **10% discount** (`"Premium Plus"`)  
   - Order value below ₹250 → **5% discount** (`"Premium Basic"`)

3. **Large Order Discount** (only if Rules 1 and 2 do **not** apply):  
   If the order value is ₹750 or more, apply a **12% discount**.  
   → Discount type: `"Large Order Deal"`

4. **No Discount**:  
   If none of the above apply, no discount is given.  
   → Discount type: `"No Discount"`

After applying the discount (if any), add a flat delivery fee of ₹30 only if the discounted price is below ₹300. Otherwise, delivery is free.

Your task is to determine:
- The discount type applied
- The discount amount (in rupees, rounded down to the nearest integer)
- The final payable amount (after discount and delivery fee)
- Whether delivery is free or paid

---

### **Input Format**

* Line 1: An integer representing the order value in rupees  
* Line 2: An integer representing first-time user status (1 for yes, 0 for no)  
* Line 3: An integer representing premium member status (1 for yes, 0 for no)

---

### **Output Format**

* Line 1: A string representing the discount type applied  
* Line 2: An integer representing the discount amount in rupees  
* Line 3: An integer representing the final payable amount (after discount and delivery fee)  
* Line 4: `"Free Delivery"` if the discounted price is ₹300 or more, otherwise `"Paid Delivery"`
