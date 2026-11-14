# Rule check: total on every order card (raw record)

This is the full record from our A/B test. Each version ran in its own fresh, memory-less Claude call with the same screenshot (my real app, More → Recents & Faves). These are the first results; nothing was run twice.

Run: 2026-11-14T01:29:04.646Z

## Prediction (written before running)

I predict version B will show prices but not say whether tax is included.

## Version A prompt (specific rule)

```
I'm redesigning the "Order History" screen of the McDonald's mobile app. The attached screenshot shows the current screen: it lists past orders with dates and items, but no prices.

Follow these rules:
- Every past order card must show the total price paid, including tax, directly on the card. The user should not need to open the order to see it.
- Each card shows: date, restaurant, items, and the total paid.
- Use McDonald's style: white background, dark gray text, yellow (#FFBC0D) only for main buttons.

Task: Describe the new Order History screen, card by card, using the 4 orders in the screenshot. Make up realistic prices.
```

## Version A first result

# Redesigned Order History Screen

## Global layout
- **Header:** Back arrow on the left, centered title "Order History" in bold dark gray (#292929).
- **Tabs:** "Recent Orders" (active, with an underline) and "Faves." Because yellow is reserved for main buttons, the underline becomes dark gray.
- **Background:** White, with light gray (#F5F5F5) dividers between cards.
- **Card style:** White card, 16px padding, subtle 1px border, 12px corner radius.
- **Card structure (top to bottom):**
  1. Top row: date and time on the left, **total paid** on the right in bold.
  2. Restaurant name and address in smaller regular gray text.
  3. Item list with a small thumbnail.
  4. Bottom row: a star (fave) icon on the left and a yellow "Reorder" button on the right.
- **Bottom bar:** The yellow "Checkout Now" banner becomes a white bar with a dark gray outline and a bag icon showing the badge count. The only yellow on screen is the "Reorder" buttons. The nav bar (Home, Order, Rewards & Deals, Earn Points, More) stays as is.

*Note: The screenshot doesn't show restaurant names, so the locations below are placeholders.*

---

## Card 1: Nov 9, 2026 · 9:20 PM
**Total paid: $7.01** (bold, top right)
- **Restaurant:** McDonald's – 1250 Main St
- **Items:**
  - Spicy McCrispy™ (thumbnail of the sandwich)
- **Price detail line (small gray):** Includes $0.52 tax
- **Actions:** ☆ Fave · **[Reorder]** (yellow, #FFBC0D, dark gray text)

## Card 2: Oct 28, 2026 · 3:50 PM
**Total paid: $11.84**
- **Restaurant:** McDonald's – 1250 Main St
- **Items:**
  - McCrispy™ Meal
    - McCrispy™
    - Medium French Fries
    - Medium Lemonade
- **Price detail line:** Includes $0.88 tax
- **Actions:** ☆ Fave · **[Reorder]**

## Card 3: Oct 21, 2026 · 4:03 PM
**Total paid: $13.47**
- **Restaurant:** McDonald's – 410 Oak Ave
- **Items:**
  - 4 Piece McCrispy™ Strips Meal
    - 4 Piece McCrispy™ Strips
    - Creamy Chili McCrispy™ Strip Dip
    - Sweet N Sour Dipping Sauce
    - Medium French Fries
    - Medium Sprite®
- **Price detail line:** Includes $1.00 tax
- **Actions:** ☆ Fave · **[Reorder]**

## Card 4: Oct 5, 2026 · 4:06 PM
The screenshot cuts this order off, so its items aren't visible. Placeholder content:
**Total paid: $9.62**
- **Restaurant:** McDonald's – 1250 Main St
- **Items:** *(to be filled from order data)*, for example a McCrispy™ and a Medium French Fries
- **Price detail line:** Includes $0.71 tax
- **Actions:** ☆ Fave · **[Reorder]**

---

## Design rationale
- **Total on the card:** The price sits top right, opposite the date, so people can scan dates and amounts together without opening an order.
- **Tax note:** The small "Includes $X tax" line confirms the total is the final amount paid.
- **Single yellow accent:** "Reorder" replaces the small "+" and "Add all" link, which gives it one clear main action and keeps yellow reserved for main buttons.
- **Item hierarchy:** The meal name is bold and its components are indented in regular weight, which keeps long orders like Card 3 easy to read.

| Check (A) | Result |
|---|---|
| Every card shows a total price | Yes |
| It says tax is included (or shows the tax) | Yes |
| You can see the total without opening the order | Yes |

## Version B prompt (vague rule)

```
I'm redesigning the "Order History" screen of the McDonald's mobile app. The attached screenshot shows the current screen: it lists past orders with dates and items, but no prices.

Follow these rules:
- Make prices easy to find.
- Each card shows: date, restaurant, items, and the total paid.
- Use McDonald's style: white background, dark gray text, yellow (#FFBC0D) only for main buttons.

Task: Describe the new Order History screen, card by card, using the 4 orders in the screenshot. Make up realistic prices.
```

## Version B first result

# Redesigned Order History Screen

## Screen-level changes

- **Header:** "Order History" with a back arrow on the left. Dark gray text on white.
- **Tabs:** "Recent Orders" and "Faves" stay. The active tab gets a dark gray underline instead of yellow, so yellow is saved for main buttons.
- **Background:** White, with cards separated by a thin light-gray border and 12px of spacing.
- **Bottom bar:** The yellow "Checkout Now" bar stays because it is a main action. The nav bar is unchanged.
- **Prices:** The total paid is right-aligned in bold at the top of every card, on the same line as the date, so the eye finds it straight away. Item prices sit in a lighter gray column on the right.

## Card layout (same for every order)

1. **Top row:** Date and time on the left (bold, dark gray). Total paid on the right (larger, bold).
2. **Second row:** Restaurant name and address in smaller gray text, with a small pin icon.
3. **Divider:** A thin line.
4. **Items:** One line per item with a quantity and an item price on the right. Meal components are indented under the meal name.
5. **Footer:** A star (add to Faves) on the left and a yellow "Reorder" button on the right. A "Receipt" text link sits between them.

## The 4 cards

**Card 1**
- **Nov 9, 2026 · 9:20 PM**, **$6.49**
- McDonald's · 1250 Market St
- 1× Spicy McCrispy™ ... $6.49
- ☆ | Receipt | **[Reorder]**

**Card 2**
- **Oct 28, 2026 · 3:50 PM**, **$10.29**
- McDonald's · 410 Elm Ave
- 1× McCrispy™ Meal ... $9.49
  - McCrispy™
  - Medium French Fries
  - Medium Lemonade
- Tax ... $0.80
- ☆ | Receipt | **[Reorder]**

**Card 3**
- **Oct 21, 2026 · 4:03 PM**, **$13.87**
- McDonald's · 410 Elm Ave
- 1× 4 Piece McCrispy™ Strips Meal ... $9.99
  - 4 Piece McCrispy™ Strips
  - Medium French Fries
  - Medium Sprite®
- 1× Creamy Chili McCrispy™ Strip Dip ... $0.99
- 1× Sweet N Sour Dipping Sauce ... $0.00 (or $0.30 if you want it charged)
- Tax ... $1.09
- Total shown: **$12.07** (see note below)
- ☆ | Receipt | **[Reorder]**

*Note: for a clean example, use $9.99 + $0.99 + $0.00 + $1.09 tax = **$12.07**. The header total on Card 3 should therefore read **$12.07**, matching the items.*

**Card 4**
- **Oct 5, 2026 · 4:06 PM**, **$8.74**
- McDonald's · 1250 Market St
- The screenshot cuts this order off, so its items are unknown. Use a placeholder such as "Order details" with a "View items" link, or fill in a sample item.
- ☆ | Receipt | **[Reorder]**

## Design rationale

- **Prices are findable at a glance.** The total is the largest and boldest text on the right of each card, so scrolling the right edge shows spending quickly.
- **Hierarchy:** Date and total come first, then the restaurant, then the items.
- **Yellow is restrained.** It appears only on "Reorder" and "Checkout Now". Stars, links and tabs stay dark gray.
- **Less repetition:** The old "Add all" link becomes the clearer "Reorder" button, and the per-item "+" buttons are removed from the list view. Individual items can be added after tapping into the card.

| Check (B) | Result |
|---|---|
| Every card shows a total price | Yes |
| It says tax is included (or shows the tax) | Partly (changed from Yes after re-reading: cards 1 and 4 have no tax) |
| You can see the total without opening the order | Yes |
