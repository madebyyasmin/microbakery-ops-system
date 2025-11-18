Micro Bakery — Inventory, Packaging & Fulfillment System

This document outlines how ingredients, packaging, and customer orders move through your micro bakery system — from stock management to production to final delivery.
It is operational logic, not database structure (that lives in notion-database-schema.md).

🍞 1. Ingredient Inventory Structure
Inventory Categories

Baking Staples (flour, sugar, salt, cocoa powder)

Sourdough Inputs (starter, flour types, water)

Mix-ins (chocolate chips, nuts, fruit)

Toppings & Finishes (icing sugar, sea salt flakes)

Packaging Materials

Café Items (milk, syrups, coffee beans)

Fields You Track per Ingredient

Item name

Category

Unit (g, kg, mL, L, units)

Current quantity

Par level (minimum acceptable quantity)

Supplier

Cost per unit

Shelf life / notes

Substitutions

Status (In Stock / Low / Out)

🗂️ 2. Weekly Stock Check Process
Every Sunday — Inventory Reset

Measure / estimate remaining stock

Update quantities in Notion

Mark any low items

Check upcoming order volume

Calculate ingredients needed for the week

Create the supplier shopping list

Every Thursday — Pre-Production Check

Reconfirm ingredient levels

Reconfirm packaging

Make adjustments for last-minute orders

🛒 3. Reordering System
What triggers a reorder:

Quantity < par level

Item manually marked “Low”

Weekly order volume requires more than what’s left

What happens next:

Item moves into the Reorder Dashboard

Status becomes Needs Reorder

Optional reminder (email or Notion notification)

Reorder notes you maintain:

Preferred supplier

Price per unit

Quality notes

Date last purchased

📦 4. Packaging Inventory
Packaging Items You Track

Cookie sleeves

Kraft boxes

Sourdough paper bags

Stickers & labels

Coffee cups + lids

Cake boards

Thank-you cards

Packaging Estimation Logic

1 sourdough loaf → 1 bread bag

6 cookies → 1 cookie sleeve

1 brownie tray → 1 kraft box

1 drink → 1 cup + 1 lid

This ensures weekly production is covered without over-ordering.

🚚 5. Fulfillment Workflow

The steps from “baked” → “packed” → “delivered/picked up”.

1. Order Approved

Payment confirmed

Order added to weekly batch

Customer listed in pickup/delivery schedule

2. Production Completed

Items baked

Quality check (appearance, weight, temperature)

Items cooled and organized by order

3. Packaging

Choose correct packaging

Add branding stickers & thank-you card

Label order (name + items)

Mark items as “Packed” in Notion

4. Pickup / Delivery

Assign pickup time window

OR assign delivery route (if offered)

Customer receives notification

Mark order as “Fulfilled”

📊 6. End-of-Week Closeout
You log:

Ingredients purchased

Leftover stock

Items sold

Waste or overages

Notes for next week (improvements, adjustments)

Outputs:

Updated cost of goods

Adjusted par levels

Trends (most popular items, high-cost weeks, etc.)

🧁 Summary

This system ensures:

ingredients never run out unexpectedly

packaging is always ready

orders move through a clean, predictable workflow

everything is trackable in Notion

operations scale smoothly as order volume grows
