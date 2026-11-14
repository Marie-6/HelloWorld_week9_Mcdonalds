# 01 Design Spec

This page holds the rules both experiences share. Mobile (page 2) is about finding the bag, past orders, and exact prices. The website (page 3) is about ordering online with a bag that syncs with the phone, and finding past orders and prices.

![01 Design Spec](../assets/01-design-spec.png)

## 01 Color

### Brand palette and roles

| Name | Hex | Role |
|---|---|---|
| McDonald's Gold | `#FFBC0D` | Hero color: primary button fill and highlights. Never use it as text on white. |
| McDonald's Red | `#DB0007` | Accent only, such as small badges and the bag count. Never use it for body copy. |
| Black | `#000000` | Type only |
| Charcoal | `#2D2D2D` | Functional: dark surfaces and icons |
| Light Gray | `#F7F7F7` | Functional: cards and section backgrounds |

### UI extension (mcdonalds.com)

| Name | Hex | Role |
|---|---|---|
| Ink | `#292929` | Default text, and the border of a selected option |
| Muted | `#7C7C7C` | Secondary text, and 1px outlines on secondary buttons, steppers and inputs |
| Divider | `#D6D6D6` | 1px lines between header, sections and rows (the mcdonalds.com header line) |
| Canvas | `#FFFFFF` | Page background and secondary button fill |
| Gold Stroke | `#C08B00` | 1px border on the primary button |
| Info Blue | `#006BAE` | Accessibility only: the keyboard focus ring. Links are Ink and underlined. |

**Allowed pairings:** Ink on Gold, Ink on White, White on Red.

**Not allowed:** Gold text on White, White on Gold.

### Lines

Every line is 1px. Which grey depends on what it does:

| Line | Color |
|---|---|
| Dividers between the header, sections and rows | Divider `#D6D6D6` |
| Outlines on secondary buttons, steppers and inputs | Muted `#7C7C7C` (keeps the 3:1 contrast controls need) |
| The selected option (chosen tab, card, radio) | Ink `#292929` |
| The primary button | Gold Stroke `#C08B00` |

Pop-ups and the bag drawer have no outline; the dimmed background separates them. Cards are Light Gray surfaces, not outlined boxes.

## 02 Typography

The brand typeface is Speedee (custom, Dalton Maag, 2018, © McDonald's). It isn't publicly licensed, so:

- **Speedee is used where it's installed.** The prototype asks the viewer's computer for Speedee first (`@font-face` with `local()`), weight by weight, and falls back to **Inter** for any weight that isn't installed. Install it on your own computer to see it, and in Figma.
- **The font file is never committed or shared.** The repo's `.gitignore` blocks font files.
- **Install Speedee Regular and Speedee Bold.** Those are the two weights the prototype uses (Light isn't used yet), so with both installed every piece of text is Speedee and the page is one family, as on mcdonalds.com: Regular for body text and unselected menu categories, Bold for headings, prices, buttons and the selected category. Without them, everything falls back to Inter.

Tracking is −0.15px. Numbers use tabular (fixed-width) figures, so prices don't change width as they change.

| Style | Size / Line height | Weight |
|---|---|---|
| Display | 36 / 40 | Bold |
| Heading | 16 / 20 | Bold |
| Body | 16 / 23 | Regular |
| Body S | 14 / 24 | Regular |
| Button | 16 / 20 | Bold |
| Caption | 10 / 14.5 | Regular |

## 03 Shape, spacing & elevation

- **Radius:** 0 for text blocks, 12 for cards and images, 48 for pill buttons.
- **Spacing:** 6, 12, 18 and 30px, and 60 (2 × 30) between menu sections. A heading always sits closer to its own content than to the section above it.
- **Elevation:** none. Separate surfaces with a divider or a Light Gray background, not a shadow. A selected state is a 1px Ink border, never a shadow.

## 04 Components

| Component | What it is |
|---|---|
| **Button** (Primary / Secondary) | A 48px pill. Primary is Gold with a 1px Gold Stroke border, and there is only one per screen. Secondary is white with a 1px Muted border. |
| **Bag Item** | One line in the bag: name, options, price, and a quantity stepper (44px tall). It can show a label such as "Added on your phone". |
| **Order Row** | One past order: date, pickup or delivery, items, restaurant, total, and "Details →". |
| **Price Summary** | Subtotal, tax, a fee line ("Fees $0.00" for pickup, "Delivery fee" for delivery), and the total. |
| **Sync Badge** | Shows "Synced", "Syncing…", or "Offline — saved on this device". |
| **Product details** | Opens over the menu (a bottom sheet on phones): name, price, calories, description, photo, "What's in it", "Your usual", then a folded **Customize** row, and a bar with quantity and "Add to bag · $X". |
| **Customize groups** | Required choices (size, meal drink) with a default already selected; optional "Remove from …" and "Extra for …" lists built from the real ingredients, each extra with its price. |
| **Location menu** | Pickup / Delivery tabs. Pickup chooses the restaurant; Delivery takes an address (or a saved one) and the restaurant it comes from. |
| **Note** | A Light Gray panel with Body S text, for one-time messages such as a price change. |

### Behavior

- **Button:** shows a pressed state within 100 ms. The label says exactly what happens, for example "Checkout · $9.34".
- **Bag Item:**
  - Changing the quantity updates the price and the total at once.
  - Setting the quantity to 0 removes the item and shows "Undo" for 5 seconds.
  - An item added on the other device shows a label until the bag is opened.
  - An item that isn't sold at the chosen restaurant stays in the bag, dimmed, with a suggested swap.
- **Order Row:** opens the order detail, which shows every item price, the tax, any fees, the total, and an "Add all to bag" button.
- **Price Summary:** is visible before checkout and in every past order, and updates live. If changing the restaurant changes the price, it says so once. Choosing delivery adds the delivery fee to the total straight away and says so once.
- **Product details:** people can read everything before deciding. Customizing is never required; the defaults let them add the item as it comes. The Customize row always shows the current choice ("As it comes", "No Butter · Extra Egg").
- **Header:** items never move. Every header slot has a fixed width, so changing text (location, sign-in name, bag count, the Gold button's price) doesn't push the others.
- **Sync Badge:** changes made offline are kept and synced later. They are never lost and never doubled.

## 05 Rule sheet

| Area | Must keep | May adapt | Must never |
|---|---|---|---|
| **Typography** | One family. The 6-step scale. Bold for headings, product names, totals, and buttons. A product's own price is Regular. Tabular figures. | Regular or Light for body text. Condensed for legal text. Display size on desktop only. | Gold or Red body text. A second typeface. Text below 10px. |
| **Color** | Gold means the primary action. Ink text on Gold. Red as a small accent only. | White or Light Gray surfaces. Where the Red count badge sits. | Gold text on white, or white text on Gold. Colors outside the palette. Gold used for anything other than the main action. |
| **Spacing & shape** | The 6 / 12 / 18px rhythm. Pill buttons and 12px cards. Flat surfaces. | Outer margins (18 on mobile, 30+ on desktop). One column on mobile, two on desktop. | Drop shadows. New radius values. Tap targets under 44px. |
| **Components** | Every price shown with its restaurant. A visible response to every tap. One Gold primary per screen. | List density and thumbnails. A drawer (web) or full screen (app) for the bag. Copy tone and length. | Removing an item without Undo. A total that hides fees until payment. |
| **Bag, orders & sync** | One bag per account, identical on web and app. Bag and orders one tap away. Past orders with item prices, tax, fees, and total. Browsing without signing in. | When to ask for sign-in. How sync is shown. Where the entry points live. | Items appearing or disappearing without notice. Losing the guest bag on sign-in. A price change that isn't shown. A button labelled "Order" that doesn't let you order. |

## 06 Platform map

| Rule | Mobile app (Task A) | Website (Task B) |
|---|---|---|
| Bag one tap away | "Bag" tab in the bottom bar, with a Red count | Bag button in the header that opens a side drawer |
| Past orders one tap away | "Orders" tab | "Orders" link in the header; list and detail side by side |
| Exact prices | Order detail screen with a Price Summary | Detail panel with a Price Summary and a receipt download |
| Same bag everywhere | Sync Badge, plus a label on items added on the website | Sync Badge, plus a label on items added on the phone |
| Sign-in | Usually already signed in | Asked at checkout only; the guest bag is kept |
| Pickup or delivery | Not covered in Task A | Location menu in the header (Pickup / Delivery); the fee shows in the bag from the first item |
| Changing an item | Not covered in Task A | Product details pop-up with a folded Customize section; "Edit" on a bag line reopens it |

## 08 Brand don'ts

- Don't put Gold text on white, or white text on Gold, in digital designs.
- Don't use Gold or Red for body copy.
- Don't use colors outside the palette.
- Don't alter the Golden Arches.
- Don't add drop shadows to UI surfaces.
- Don't commit, upload or share the Speedee font file. Install it locally.
