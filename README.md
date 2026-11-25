# Smart India Hackathon Workshop
# Date: 25.11.2026
## Reference Number: **26017589**
## Name: **Janesh.M**

## Problem Title
SIH 26033: Multiple intermediaries reduce farmers' earnings and increase consumer prices.

## Problem Creator's Organization
Ministry of Consumer Affairs, Food & Public Distribution

## Theme
Agriculture, FoodTech & Rural Development

## Problem Description
Farmers often sell their crops through several middlemen. Because of this, farmers may receive a low price while the same products reach customers at a much higher price. It can also be difficult for farmers to know how much quantity buyers need before harvesting.

## Proposed Solution
FarmSync is built on one simple idea: sell before you harvest. Instead of carrying crops to the market and hoping to find a buyer, farmers announce what will be ready, and nearby shops, hotels, supermarkets and local customers reserve it directly.

How it works:
1. List expected harvest: The farmer adds the crop, approximate quantity and harvest date, with a confidence tag (Sure / Likely / Weather-dependent) so buyers know how firm the quantity is.
2. Post buyer demand: Buyers post the crop, quantity, date and delivery area they need.
3. Smart matching: Each request is scored against nearby farmers' listings by crop, distance, date window and quantity.
4. Group into Sync Points: Small orders from nearby buyers are combined into one larger order with a common pickup point (a "Sync Point") at a fixed day and time, so one trip serves many buyers.
5. Fair Price Band: Instead of one fixed price, the app shows a range between the recent local mandi price and the retail price. Farmer and buyer agree on a price inside this range, so the farmer earns more than the mandi rate and the buyer pays less than retail. (Example: mandi Rs 18/kg, retail Rs 30/kg, agreed Rs 24/kg.)
6. Confirm and pay advance: The farmer confirms quantity and price, and the buyer pays a small UPI advance that is held until delivery.
7. Pickup and delivery: Local transport carries the order to the Sync Point for collection. A quality grade (A/B/C) and a photo are recorded at pickup.
8. Payment and ratings: The advance is released on delivery, and farmer and buyer rate each other. The grade and photo help settle any dispute.
The main feature of FarmSync is a **Harvest Planner**. Farmers can add the crops they expect to harvest, the approximate quantity and the harvest date. Buyers can post what they need and when they need it. FarmSync matches these requests with nearby farmers. It can also combine smaller orders from nearby buyers into one larger order, so farmers can sell more quantity in a single trip.

## Technical Approach
I would start by making a simple website and later improve it into a mobile app.

- Frontend: HTML, CSS and JavaScript.
- Backend: Python (Flask) with MySQL to store farmers, buyers, crops, listings and orders.
- Matching: a score based on crop, distance, date window and quantity. Nearby buyer orders are grouped using a location clustering method such as DBSCAN to form group orders and Sync Points.
- Mapping: A map service to show nearby farms, pickup points and delivery locations.
- Pricing: recent local mandi prices from AGMARKNET data form the base of the Fair Price Band.
- Demand prediction: a simple model (moving average or regression) on past orders and seasonal demand to show which crops may be needed more.
- Notifications: SMS/WhatsApp alerts for new matches and changes.
- A basic prediction model can use previous orders and seasonal demand to estimate which crops may be needed more. Route planning can help choose a suitable delivery path.

**Working flow:**
<img width="3200" height="1817" alt="farmsync_working_flow (1) (1)" src="https://github.com/user-attachments/assets/9c678d94-f86b-4182-92f0-660cf5da6b8c" />


## Feasibility and Viability
FarmSync can first be tested in one nearby area with a few farmers and shops. It does not need its own vehicles because local transport services can be used. The main challenge is that harvest quantity can change because of weather or other reasons. Farmers can update stock and harvest date at any time, and matched buyers are notified immediately. If a farmer cannot fulfil an order, FarmSync re-matches it to another nearby farmer, and the buyer's advance is returned if no match is found. The service can stay free for farmers, with a small service fee from buyers once it is running.

## Impact and Benefits
- Farmers can find buyers directly and reduce their dependence on middlemen.
- Buyers can compare prices and purchase from nearby farms.
- The Harvest Planner helps farmers understand demand before harvesting.
- Group orders and shared pickup points can reduce transport costs.
- Better demand information may help reduce unsold crops and food waste.

## Research and References
1. e-NAM - https://www.enam.gov.in/
2. Small Farmers' Agribusiness Consortium - https://sfacindia.com/
3. AGMARKNET - https://agmarknet.gov.in/
