# 02 Mobile — Task A

**Find my bag, past orders, and exact prices.** This page uses the Design Spec from page 1.

![02 Mobile](../assets/02-mobile.png)

## 01 Context pack

**Person & task**
A grad student who orders breakfast in the McDonald's app before class. They want to see what's in their bag, find what they ordered last time, and see exactly what it cost.

**Observation**
> "In the app I couldn't find a bag, my past orders, or the price I actually paid. I had to rebuild my usual order from the menu every time." (my own attempt, Nov 2026)

**Assumptions to check**

1. People look for past orders in the bottom tab bar, not inside Account.
2. People want to see the price they paid, not only today's price.
3. Breakfast is often the same order, so "Order again" saves the most time.

**Test:** ask a classmate to find the total of their last order. Time it, and note where they tap.

## 02 Mobile rules

| Must keep | May adapt | Must never |
|---|---|---|
| Bag and Orders are tabs in the bottom bar on every screen. | Tab order and icons. | Hiding Orders inside Account or Profile. |
| The bag shows the restaurant, pickup time, and total before checkout. | An "Order again" card on Home. | Showing a total without tax. |
| Every past order opens to item prices, tax, and total. | How many recent orders Home shows (2–3). | Emptying the bag when someone browses past orders. |

**Component:** Tab Bar (mobile), with Active = Home, Bag, or Orders. The Red badge shows the bag count and is the only Red on the screen.

## 03 Real app today (before)

I checked our design against the real McDonald's app on my own phone (Nov 13, 2026). Section 03 of the image shows my screenshots as evidence.

1. With an empty bag, there is no bag icon anywhere on the home screen.
2. After adding one item, a yellow "Checkout Now" bar appears above the tabs.
3. The same bag has three names: "Add to Bag", "Checkout Now" and "Your order".
4. The bag page shows only the subtotal. There is no tax and no total.
5. Past orders are under More → Recents & Faves. They show dates and items, but no prices.
6. The Order tab has a second list ("Quickly reorder"), also with no prices.

## 04 Our redesign (after)

The "Menu" tab is now called "Order", like the real app. Screens use my real restaurant and past orders. Prices we add are illustrative, because the real app does not show what I paid.

1. **Home:** Bag and Orders are tabs, never buried. "Order again" shows the last order (Spicy McCrispy™) and the price paid ($6.28).
2. **Bag:** called "Your bag" everywhere. It shows the restaurant, pickup time, tax and full total before checkout. The item added on the website is labelled. The button reads "Checkout · $11.60".
3. **Orders:** every past order shows its date, restaurant and the total paid, tax included.
4. **Order detail:** shows each item price, the tax and the total ($10.23). "Add all to bag" keeps the real app's "Add all" idea.
