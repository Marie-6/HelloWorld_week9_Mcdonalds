# McDonald's — One System, Two Experiences

**SVA MFA IxD · Assignment 2 · Context and evidence study**

This is a small design system for McDonald's ordering. Two platforms share one set of rules:

| Page | Task |
|---|---|
| [01 Design Spec](docs/01-design-spec.md) | Type, color, spacing, radius, reusable components, and the rule sheet (must keep / may adapt / must never) |
| [02 Mobile — Task A](docs/02-mobile.md) | Find the bag, past orders, and exact prices in the app |
| [03 Website — Task B](docs/03-website.md) | Order online, keep one bag synced with the phone, and find past orders with prices |

![01 Design Spec](assets/01-design-spec.png)
![02 Mobile](assets/02-mobile.png)
![03 Website](assets/03-website.png)

## Website prototype

**[Try it → marie-6.github.io/Mcdonalds/website/](https://marie-6.github.io/Mcdonalds/website/)**

A working redesign of the mcdonalds.com breakfast menu, built from the Design Spec and the Website rules (page 3). It keeps the real site's menu layout (category rail with photos, centered product grid) and header (Our Menu, Meal Deals, Search, location, Order Now), and adds ordering on the site, for pickup or delivery (address, a delivery fee shown in the bag before checkout, drop-off notes). Every item opens a product pop-up over the menu: details and "What's in it" first, ready to add as it comes, with a folded "Customize" section to change it (size, meal drink, "Remove" and "Extra" options from the real ingredient lists, and "Your usual" from your own order history); the options follow the item into the bag, checkout, orders and receipt. You can order for pickup, keep one bag (sign in at checkout to merge the bag from your phone), switch restaurants and see prices update, and find past orders with item prices, tax, total, "Add all to bag" and a downloadable receipt. Nothing is really ordered or paid. **Type:** the page uses McDonald's Speedee typeface *if it's installed on your computer*, and Inter otherwise. Speedee isn't publicly licensed, so the font file is never committed here (see `.gitignore`); install it locally to see it. Source: [`website/index.html`](website/index.html).

Product photos and the Golden Arches logo come from the mcdonalds.com breakfast and McCafé menus (`website/img/`), used unaltered for this student exercise.

## The core idea

> The design system carries the rules that do not change.

Both experiences are checked against one rule sheet:

- **One bag per account.** It is identical on the web and in the app: same items, same restaurant, same price.
- **The bag and past orders are always one tap or click away.**
- **Every price is shown with its restaurant.** Past orders list each item price, the tax, any fees, and the total.
- **Never** show a button labelled "Order" that doesn't let you order.
- **Never** let items appear or disappear without notice.

## Files

- `docs/` — the spec for each page, as text
- `assets/` — PNG exports of the three Figma frames
- Figma source: frames `01 Design Spec`, `02 Mobile — Task A`, `03 Website — Task B`

## Sources

- McDonald's *Feel-Good Design Cheatsheets* v1.2 (Sept 2019)
- UI values from mcdonalds.com, as captured by [shadcn.io/design/mcdonalds](https://www.shadcn.io/design/mcdonalds)
- Speedee typeface: [Fonts In Use](https://fontsinuse.com/typefaces/231234/speedee). Prototypes use Inter as a stand-in.

*Prices are illustrative. McDonald's, the Golden Arches, and Speedee are trademarks of McDonald's. This is a student design exercise and is not affiliated with McDonald's.*
