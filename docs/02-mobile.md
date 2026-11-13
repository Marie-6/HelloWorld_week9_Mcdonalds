# 02 Mobile — Task A

**Find my bag, past orders, and exact prices.** This page uses the Shared System from page 1.

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

## 03 Screens

1. **Home:** Bag and Orders are tabs, never buried. "Order again" shows the last order and the price paid ($9.34).
2. **Bag:** shows the restaurant, pickup time, and full total before checkout. The item added on the website is labelled. The button reads "Checkout · $7.60".
3. **Orders:** lists every past order with its date, restaurant, and the total paid, tax included.
4. **Order detail:** shows each item price, the tax, and the total. "Add all to bag" says whether today's price is different.
