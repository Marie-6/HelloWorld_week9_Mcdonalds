# McDonald's website: Task B

## Short note (Marie, web)

**Observation.** I observed my own attempt to order breakfast on mcdonalds.com from my laptop. The site only let me browse, "Order Now" sent me to the app, and I could not find what I paid for my last order.

**Decision and reason.** I observed that the website could not take an order, so I changed it to order for pickup or delivery, share one bag with the phone app, and show past orders with a receipt, because a person working on a laptop should not have to pick up their phone, and should be able to see what they paid. I kept the real site's menu layout, photos, logo and the spec's colors, because the ordering flow was broken, not the brand.

**Preserved rule.** One bag per account. It is identical on the web and in the app: same items, same restaurant, same price.

**Prediction and check.** We predicted that a vague rule ("Make prices easy to find") would show prices but not say whether tax is included. Checked: partly true, 2 of 4 order cards had no tax. So we kept the specific rule: every past order shows item prices, tax and total. Full record: [rule-check-results.md](../docs/rule-check-results.md).

**My contribution.** The web task (Task B): the observation, the person and task, and the design decisions, such as a product pop-up instead of a full page, pickup and delivery, and sign-in only at checkout. Aria did the mobile task. We wrote the rule sheet together.

**AI and source help.** Claude (Claude Code) built `index.html` from my prompts and our Design Spec. Every prompt is in [prompt.md](prompt.md), word for word, and my decisions are in [process.md](process.md). Layout, photos and logo come from mcdonalds.com. Color and type values come from McDonald's *Feel-Good Design Cheatsheets* v1.2.

**One remaining question.** Will a person on a laptop sign in at checkout if it means their bag and past orders also show up on their phone? I have only tested this on myself, not with a classmate yet.

---

The [McDonald's website](https://www.mcdonalds.com/us/en-us/full-menu/breakfast.html) only lets you browse the menu, and the app hides your bag, past orders and what you actually paid. So we redesigned both, starting with the cart and the receipt. On the website, you can now **order on your laptop** for pickup or delivery, the **bag stays in sync** between the website and the app, and you can **find past orders** with every item's price, the tax and the total in one step.

**Try it:** [marie-6.github.io/HelloWorld_week9_Mcdonalds/website](https://marie-6.github.io/HelloWorld_week9_Mcdonalds/website/) · with the app side by side: [demo](https://marie-6.github.io/HelloWorld_week9_Mcdonalds/demo/)

## What you can do

- **Order on a laptop:** browse the breakfast menu, customize items, and check out for pickup or delivery
- **Cart:** one bag shared with the app, with every price, the tax and any fee shown before checkout
- **Receipt:** every past order lists item prices, tax and total in one place; download it or add it all to the bag again

## Built on

- [Design Spec](../docs/01-design-spec.md) (colors, type, spacing, components, rules)
- [Website task and rules](../docs/03-website.md)

## Font

Designed in **Speedee** (McDonald's typeface). It isn't publicly licensed, so it's not in this repo: install Speedee Regular and Bold on your computer to see it. Without them the page shows Inter.

## Files

- `index.html`: the whole prototype
- `img/`: product photos and logo (© McDonald's)
- [prompt.md](prompt.md): every prompt and decision
- [process.md](process.md): how it changed, with before/after pictures

*Student prototype (SVA MFA IxD), not affiliated with McDonald's. Nothing is really ordered or paid. Prices are illustrative.*
