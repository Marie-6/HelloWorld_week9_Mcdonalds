# McDonald's — One System, Two Experiences

**SVA MFA IxD · Assignment 2 · Context and evidence study**

This is a small design system for McDonald's ordering. Two platforms share one set of rules:

| Page | Task |
|---|---|
| [01 Shared System](docs/01-shared-system.md) | Type, color, spacing, radius, reusable components, and the rule sheet (must keep / may adapt / must never) |
| [02 Mobile — Task A](docs/02-mobile.md) | Find the bag, past orders, and exact prices in the app |
| [03 Website — Task B](docs/03-website.md) | Order online, keep one bag synced with the phone, and find past orders with prices |

![01 Shared System](assets/01-shared-system.png)
![02 Mobile](assets/02-mobile.png)
![03 Website](assets/03-website.png)

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
- Figma source: frames `01 Shared System`, `02 Mobile — Task A`, `03 Website — Task B`

## Sources

- McDonald's *Feel-Good Design Cheatsheets* v1.2 (Sept 2019)
- UI values from mcdonalds.com, as captured by [shadcn.io/design/mcdonalds](https://www.shadcn.io/design/mcdonalds)
- Speedee typeface: [Fonts In Use](https://fontsinuse.com/typefaces/231234/speedee). Prototypes use Inter as a stand-in.

*Prices are illustrative. McDonald's, the Golden Arches, and Speedee are trademarks of McDonald's. This is a student design exercise and is not affiliated with McDonald's.*
