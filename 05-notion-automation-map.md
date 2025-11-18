# ⚙️ Automation Map — Micro Bakery OS (Notion)

This file documents all automations used across the bakery system.  
Each automation references entities defined in the schema but does not repeat their structure.

---

# 1. Order Intake Automations

### **A. New Order → Production Schedule**
Trigger: New entry added to “Orders”  
Action: Create linked Production Schedule entry  
Outcome: Production timeline updates automatically.

### **B. Mark Order as Completed → Update Finance**
Trigger: Status changes to “Completed”  
Action: Log revenue in Finance Tracker  
Outcome: Weekly totals stay accurate.

---

# 2. Menu Planning Automations

### **A. Activate Weekly Menu → Filter Production List**
Trigger: Check “Active This Week?”  
Action: Show items in production planning  
Outcome: Only current menu items appear in weekly views.

### **B. Seasonal Tags → Suggested Specials**
Trigger: Category + Tag combination  
Action: Create suggestion card in menu planning  
Outcome: Faster planning of new limited-time items.

---

# 3. Inventory Automations

### **A. Low Stock Alert**
Trigger: Stock level < threshold  
Action: Add card to “Restock” view  
Outcome: No more missing ingredients.

### **B. Produce Item → Deduct Inventory**
Trigger: Production entry marked as “Completed”  
Action: Subtract ingredient quantities from inventory  
Outcome: Stock levels stay accurate.

---

# 4. Finance Automations

### **A. Weekly Summary**
Trigger: Every Sunday evening  
Action: Roll up weekly totals → Summary Page  
Outcome: Finance stays organized for tax prep.

### **B. Monthly Close**
Trigger: Last day of month  
Action: Generate new “Monthly Report” page  
Outcome: Clean separation of each month’s numbers.

