# 📊 Notion Database Schema — Micro Bakery OS

This file defines every database used in the bakery’s Notion system.  
No workflows and no automation logic are included here — only structure.

---

# 🗂 1. Orders
Tracks every customer order.

**Fields**
- Order ID (formula or auto-number)
- Customer Name (text)
- Items Ordered (relation → Menu Items)
- Quantity (number)
- Pickup/Delivery Date (date)
- Total Price (formula)
- Status (select: New, In Production, Ready, Completed)
- Payment Status (select: Paid, Unpaid)
- Notes (text)

---

# 🍞 2. Menu Items
Core menu for sourdough, cookies, cakes, brownies.

**Fields**
- Item Name (text)
- Category (select: Sourdough, Cookies, Cakes, Brownies)
- Base Price (number)
- Ingredient List (relation → Ingredients)
- Production Time (number, hours)
- Active This Week? (checkbox)
- Photo (file)

---

# 🧂 3. Ingredients
Simple inventory management.

**Fields**
- Ingredient Name (text)
- Category (select: Dry, Wet, Dairy, Other)
- Unit Cost (number)
- Stock Level (number)
- Unit Type (select: g, ml, pieces)
- Supplier (text)
- Linked Items (relation → Menu Items)

---

# 🗓 4. Production Schedule
Daily batching + timing.

**Fields**
- Production Date (date)
- Item (relation → Menu Items)
- Quantity to Make (number)
- Start Time (time)
- End Time (time)
- Linked Orders (relation → Orders)

---

# 💰 5. Finance Tracker
Basic revenue + cost overview.

**Fields**
- Date (date)
- Revenue (number)
- Ingredients Cost (number)
- Supplies Cost (number)
- Profit (formula)
- Notes (text)

