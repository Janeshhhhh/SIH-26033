# Smart India Hackathon Workshop
# Date: 24.11.2026
## Reference Number: 26017589
## Name: Janesh.M

## Problem Title
SIH 26033: Multiple intermediaries reduce farmers' earnings and increase consumer prices.

## Problem Creator's Organization
Ministry of Consumer Affairs, Food & Public Distribution

## Theme
Agriculture, FoodTech & Rural Development

## Problem Description
Farmers often sell their crops through several middlemen. Because of this, farmers may receive a low price while the same products reach customers at a much higher price. It can also be difficult for farmers to know how much quantity buyers need before harvesting.

## Proposed Solution
My app idea is called **FarmSync**. It is a platform that connects farmers directly with shops, hotels, supermarkets and local customers.

The main feature of FarmSync is a **Harvest Planner**. Farmers can add the crops they expect to harvest, the approximate quantity and the harvest date. Buyers can post what they need and when they need it. FarmSync matches these requests with nearby farmers. It can also combine smaller orders from nearby buyers into one larger order, so farmers can sell more quantity in a single trip.

The app can show a suggested price using recent local market prices as a reference. It can also group orders by area and suggest a common pickup point. This helps farmers plan before taking their crops to the market and helps buyers avoid unnecessary extra costs.

## Technical Approach
I would start by making a simple website and later improve it into a mobile app.

- HTML, CSS and JavaScript for the website pages.
- Python for matching buyer requests with nearby farmers and available crops.
- MySQL to store farmer, buyer, crop and order details.
- A map service to show nearby farms, pickup points and delivery locations.
- A basic prediction model can use previous orders and seasonal demand to estimate which crops may be needed more. Route planning can help choose a suitable delivery path.

**Working flow:**
<img width="1672" height="941" alt="07d1be48-b957-4624-ab0f-b38721f728f1" src="https://github.com/user-attachments/assets/9f0a8d09-89f0-450c-aa44-f12e4e08125f" />



## Feasibility and Viability
FarmSync can first be tested in one nearby area with a few farmers and shops. It does not need its own vehicles because local transport services can be used. One challenge is that the actual harvest quantity may change due to weather or other reasons. Farmers should be able to update their stock and harvest date so buyers receive correct information.

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
