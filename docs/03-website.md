# 03 Website — Task B

This page covers ordering online with one bag on every device, and past orders with prices. It uses the Design Spec from page 1. Prices are illustrative.

![03 Website](../assets/03-website.png)

## 01 Context pack

**Person & task**

A grad student on a laptop who wants breakfast without picking up their phone. They already use the McDonald's app. The task: order on the website for pickup or delivery, have the same bag on the phone, and find past orders with what they cost.

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
| "Orders" is in the header on every page, at every screen size. | | Showing a price without its restaurant. |
| Pickup or delivery is chosen in the header and shown there. | Where the restaurant list sits in the location menu. | Adding the delivery fee only at payment. |
| Product details come before any choice; customizing is optional. | How many options show before "Customize" is opened. | Forcing a choice before the item can be added. |
| Header items keep their place whatever changes. | Labels as icons on narrower screens. | A header that shifts when the total, location or name changes. |

**Components:**

- **Web Header** (Active = Menu or Orders): logo, Our Menu, Meal Deals, Orders, More; then Search, the location (Pickup · restaurant or Delivery · street), account, Bag (a fixed-width button with its contents centered; the count appears from the first item), and one fixed Gold slot ("Order Now" with an empty bag, "Checkout · $X" with items). Under 1300px it becomes logo, Search, Orders, Bag and a menu button.
- **Category Rail:** the menu categories with photos, in a Light Gray panel; the current one is bold with a Red bar.
- **Menu Card:** photo, name (Bold) and price at the selected restaurant (Regular), with a direct "Add to bag". McDonald's photos leave empty space above the food, so each category's photo frame is cut just above its tallest item's food (bottom-aligned): no food is cropped, every photo in a row keeps the same scale, and the title sits close to its products. Clicking the photo or name opens Product details.
- **Product details**, **Customize groups** and **Location menu:** see the Design Spec, 04 Components.

## 03 Screens

The Figma frame above is the first version. The working prototype is the current one: [marie-6.github.io/Mcdonalds/website](https://marie-6.github.io/Mcdonalds/website/).

1. **Menu:** the Category Rail on the left and Menu Cards on the right, starting with Breakfast Meal Deals. Every item shows its price at the chosen restaurant and has an "Add to bag" button. A toast confirms the click ("Synced with your phone") and the bag count updates.
2. **Product details:** opens over the menu. Details and "What's in it" first, "Your usual" if you've ordered it before, then a folded Customize section. "Add to bag · $X" works straight away.
3. **One bag with the app:** in the prototypes, the website and the app keep one bag in the browser, so an item added on either shows up on the other right away (see them side by side on the [demo page](https://marie-6.github.io/Mcdonalds/demo/)). Items are labelled "Added on your phone" / "Added on the website" until the bag is opened.
4. **Location menu:** Pickup or Delivery. Delivery asks for an address and adds the delivery fee to the bag total at once.
5. **Bag drawer:** the same bag as in the app. The item added on the phone is labelled. The drawer shows pickup (restaurant, time) or delivery (address, restaurant, time), each item's options with an Edit link, and the full total including any fee. The button reads "Checkout · $9.34".
6. **Sign in at checkout:** sign-in is only asked for here, never before browsing. The guest bag stays as it is. Signing in syncs the bag with the app and unlocks past orders.
7. **Checkout:** pickup at / deliver to (with drop-off notes), time, payment on pickup or on arrival, and the order summary with "Place order · $X".
8. **Orders:** the same history as in the app, each marked Pickup or Delivery. The list is on the left; the selected order is on the right, with every item price and option, the tax, any fee, and the total. It also has "Add all to bag" and "Download receipt" buttons.
