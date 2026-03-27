# Delivery-Store
In this repository we understand how the delivery store were design. What is high-level and low-level design look like of such a system

Functional Requirements:
1. Customer is able to search the items and availability based upon it's location and delivery duaration is within 1 hour.
2. Customer is able to order the items

Non-Functional Requirements:
1. Latency: When customer search for items and their availability end to end time should be minimal.
2. Consistency: For a specific item there might be a case multiple customer want to buy a item, in that case consistency matters. For that we acquire a lock using reddis.

Core Entites:
1. Item --- Item_id, name, description
2. Inventory-- Store name, item_id, quantity
3. Distribution center--inventory_name, coordinates
4. order--order_id,status(based upon payment)
5. Order_Item--user_id, deliverable_item

Api designing:


