# 03 Website — Task B

This page covers ordering online with one bag on every device, and past orders with prices. It uses the Shared System from page 1. Prices are illustrative.

![03 Website](../assets/03-website.png)

## 01 Context pack

**Person & task**

A grad student on a laptop who wants breakfast without picking up their phone. They already use the McDonald's app. The task: order for pickup on the website, have the same bag on the phone, and find past orders with what they cost.

**Observation**

> "On mcdonalds.com I could only browse. 'Order Now' pushed me to the app, so I ordered through DoorDash instead. I couldn't see what things cost or what I ordered before." (my own attempt, Nov 2026)

**Assumptions to check**

1. Desktop users who click "Order Now" expect to order on the site.
2. People will sign in at checkout if it syncs the bag and shows past orders.
3. People expect the same bag on phone and laptop.

**Test:** give a classmate only the URL and ask: "Order an Egg McMuffin for pickup, then find what you paid last time." Note where they click and where they get stuck.

## 02 Website rules

| Must keep | May adapt | Must never |
|---|---|---|
| "Order Now" lets you order on this site. | A drawer on wide screens, a full bag page on narrow ones. | Sending desktop users to an app store to order. |
| The Bag button in the header shows a count on every page. | Asking for sign-in at checkout, or when the user chooses to sync. | Asking for sign-in before browsing or adding to the bag. |
| The bag drawer shows the restaurant, the items, and the full total. | Orders list and detail side by side, stacked when the screen is narrow. | Losing the guest bag on sign-in. |
| "Orders" is in the header on every page. | | Showing a price without its restaurant. |

**Components:**

- **Web Header** (Active = Menu or Orders): the Bag count and Orders appear on every page, and the restaurant is always visible.
- **Menu Card:** shows the item's price at the selected restaurant, with a direct "Add to bag" button.

## 03 Screens

1. **Menu:** every item shows its price at the chosen restaurant and has an "Add to bag" button. A toast confirms the click ("Synced with your phone") and the bag count updates.
2. **Bag drawer:** the same bag as in the app. The item added on the phone is labelled. The drawer shows the restaurant, pickup time, and full total. The button reads "Checkout · $9.34".
3. **Sign in at checkout:** sign-in is only asked for here, never before browsing. The guest bag stays as it is. Signing in syncs the bag with the app and unlocks past orders.
4. **Orders:** the same history as in the app. The list is on the left; the selected order is on the right, with every item price, the tax, and the total. It also has "Add all to bag" and "Download receipt" buttons.
