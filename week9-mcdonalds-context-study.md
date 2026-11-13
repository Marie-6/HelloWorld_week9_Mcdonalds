# One System, Two Experiences: McDonald's App and Website

**Week 9 · Assignment 2 · Context and Evidence Study**
**Team:** Aria (mobile) · Marie (web)

---

## 1. Person and Task

Both of our tasks are for the same kind of user: a student who often orders McDonald's, wants to save money, and already uses the app.

### Mobile (Aria)

**Person:** A student who orders on the phone and wants to keep track of how much they spend.

**Task:** Find the bag (cart), and find the price of an old order.

**What I saw:** When I used the McDonald's app, it was hard to find the bag. It was also hard to find how much I paid for my last order.

**Other evidence:** The bag icon only shows up after you add something. Online guides use different names for the old orders page, like "Recents," "Orders," or "My Account." Some guides also say the order details page is not the same as the receipt.

**What we want to check**
1. Users can only understand the bag is the cart if it is always on the screen, even when it is empty.
2. Users look for old orders under "Account" or "History," not "Recents."

### Web (Marie)

**Person:** A grad student who is working on a laptop and wants breakfast, but does not want to pick up their phone. They are already logged in to the app on their phone.

**Task:** On mcdonalds.com, pick a breakfast item, add it to the bag, and check out for pickup. The same bag also shows up in the phone app, so they can finish or change the order there.

**What I saw:** "I opened the breakfast menu on mcdonalds.com to order. The site only lets me browse. 'Order Now' pushed me to the app, and I only got food because I thought of DoorDash myself. I couldn't find my past orders or prices either."

**Other evidence:** In the U.S., you can only order delivery on the website, and it uses a separate site run by DoorDash. So website orders and app orders are saved in different places.

**What we want to check**
1. People on a laptop who click "Order Now" think they can order on the website.
2. People will log in on the laptop if it means their bag and old orders also show up on their phone.
3. People think the bag should be the same on both devices: same items, same restaurant, same price.

---

## 2. Shared Rule Sheet

Our shared rules are in our Figma file, **McDonald's Design Spec — Order Flow**. It has color, type, spacing, components, the rule sheet (must keep / may adapt / must never) and interaction rules. Both of our tasks follow it.

---

## 3. Our Design

### Mobile: Find the bag and old prices (Aria)

**Before:** The bag only shows up after you add an item. To see the price of an old order, you need to tap many times.

**After:**
- The Bag tab is always in the bottom bar, with a number on it (it shows 0 when empty).
- There is an "Order History" button in the bottom bar. Each order card shows the date, the restaurant and the total price, so you don't need to open the order.
- Items added on the website have a small label: "Added on your computer."

### Web: Order on the website with a synced bag (Marie)

Desktop, 1440px.

| Frame | What it shows |
| --- | --- |
| 1. Before | The menu page today. "Order Now" sends you to the app, and there is no bag. |
| 2. Menu + Add to bag | Every item card has an "Add to bag" button. The top bar shows a bag icon with a number. |
| 3. Bag panel | Opens on the right side. At the top: restaurant and pickup time. Then the items, the total price, and "Checkout." |
| 4. Log in | Shows up at checkout: "Sign in to check out and sync this bag with your app." The items in the bag are not lost. |
| 5. Synced | Phone and laptop side by side, with the same bag. One item has the label "Added on your phone." |
| 6. Special case | The user changes the restaurant, and the hash browns are not sold there. The item stays in the bag in grey, with a suggestion to swap it, and the new total is shown. |
| 7. Order history | Old orders as cards, and each card shows the total price. They are the same orders as on the phone. |

---

## 4. Decisions

**Aria:** I saw that the bag only showed up after I added an item, so I changed it to a Bag tab that is always there with a number, because people can't use a cart if they can't find it.

**Aria:** I saw that the price of an old order was hidden behind many taps, so I put the total price on each order card, because people should not have to open every order just to check the price.

**Marie:** I saw that "Order Now" on the website sent me to the app instead of letting me order, so I changed the website so you can order there, with a bag that syncs with the phone, because a button should do what it says.

**Marie:** I kept McDonald's name "Bag" and did not change it to "Cart," because the problem was that people couldn't see it, not the name. Also, the name needs to be the same on both devices.

---

## 5. Who Did What

| | Aria | Marie |
| --- | --- | --- |
| Work | Mobile bag and order history; research on the app's cart and old orders; this write-up | Website ordering, synced bag and order history; Figma design spec and rule sheet |
| Sources | McDonald's U.S. website and help pages; news about McDonald's and DoorDash website ordering (August 2025); online guides about the app's bag and order history | Our own tests on mcdonalds.com and the app |

**Question we still have:** Will people really log in on a laptop to sync their bag? Or will they skip logging in and lose the link to their phone?
