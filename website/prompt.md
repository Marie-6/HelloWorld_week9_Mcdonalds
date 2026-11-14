# Prompts: McDonald's website (Task B)

Every prompt Marie gave Claude (Claude Code) for this project, in order and word for word (typos kept), with what was done and the decisions Marie made. The process, with before/after pictures, is in [process.md](process.md).

**Key:** ✅ done as asked · 🔁 needed a second try · ✋ not done as asked (the reason is given)

---

### Setting up the repo

**1.** "can you create week9-Mcdonald's file in github and share it with xhang1@sva.edu so that we can all have access to that file"
- Made a `week9-Mcdonald's` folder in the class repo (hello-world) and invited Xinyu's account (AriaHang) as a collaborator. ✅

**2.** "i dont want her to have access to edit other files, and she need to publish it. so maybe delete this file"week9" and her access, create a new whole page file called"Mcdonald's" and invite her to that folder"
- Removed Xinyu from hello-world and deleted the folder. Created a separate repo, **Marie-6/Mcdonalds**, with GitHub Pages, and invited only her. ✅
- **Decision (Marie):** keep McDonald's in its own repo so Xinyu can publish without touching other class work.

**3.** "contributors should have her"
- Explained that GitHub lists contributors from commits, so she appears after her first push. She did. ✅

**4.** "so can she see this folder at her github?"
- Yes: through the direct link and her dashboard, but not under her profile's Repositories, since Marie owns the repo. ✅

### Design spec files

**5.** "https://www.figma.com/design/469E5OWXWwcozEdOPqvCVs/Untitled?node-id=6-2… push this part to github "mcdonalds"" (+ screenshot of the 3 frames)
- Figma had to be connected first. 🔁

**6.** "ok try again"
- The Figma file was view-only for Marie's account, so it couldn't be read. Asked for an export instead. 🔁

**7.** "/Users/marie/Downloads/01-shared-system.md /Users/marie/Downloads/02-mobile.md /Users/marie/Downloads/03-website.md /Users/marie/Downloads/README.md push these to github"
- Pushed the spec into `docs/` with the README. The site now shows the README. ✅

**8.** "/Users/marie/Downloads/Untitled.zip there are the pics"
- Added the three Figma frame PNGs to `assets/`. ✅

**9.** "change to this one" (+ new Design Spec frame)
- Replaced the page 1 image. ✅

**10.** "yes, and the one on github should change too"
- Renamed "Shared System" to "Design Spec" in the text and file names. ✅

### Building the website

**11.** "according to these desgin specs and rules, redesign the website https://www.mcdonalds.com/us/en-us/full-menu/breakfast.html  make sure it can take oders and add them to cart and find history/ reciept after" (+ Design Spec image, 03-website.md)
- Built `website/index.html`: breakfast menu, bag drawer, sign-in at checkout, checkout, order history, and downloadable receipts. ✅

**12.** "can you add the product's photo? you can find them on the website, make sure there's logo and all design follows the design spec. you can use https://www.doordash.com/store/mcdonalds-jersey-city-837556/1197420/ for example"
- Added real product photos and the Golden Arches from mcdonalds.com and swapped out photos that had promo badges. Removed calorie numbers that had been guessed. ✅

**13.** "https://www.mcdonalds.com/us/en-us/full-menu/extra-value-meals-menu.html you didnt keep the design of the product menus … and the bar menu maybe should have more function?"
- Rebuilt the menu in the real site's layout: category rail with photos, centered titles, large photos. Added Breakfast Meal Deals. The header gained Our Menu, Meal Deals, Orders, More, Search, location and Order Now. ✅

**14.** "and maybe it should have product page for people to custmize? https://www.doordash.com/… you can still use this for example"
- Product page with size and meal-drink choices, plus Remove/Extra lists built from the real ingredient lists. Options carry into the bag, orders and receipt. Replaced DoorDash's made-up "ordered by 10+ others" with **"Your usual"** from your own history. ✅

**15.** "maybe the product page can just jump out first, but not the whole page … doordash jump out like this, but you can change that. just make sure people can scan the details first and give them chance to hesitate before making the customize decisions"
- Made it a pop-up over the menu (a bottom sheet on phones). Details come first, defaults are preselected, and **Customize is folded**. ✅

### Fixing against the design rules

**16.** "why everything has a black liner outside the box?"
- The dark outlines on pop-ups, the drawer and menus were my workaround for "no shadows". Replaced them with the spec's light divider or Light Gray surfaces. ✅

**17.** "why the head bar, stuff is drifting when i add more numbers to the bag?"
- The gold "Checkout · $X" button changed width as the price changed. Made all digits fixed-width and gave the button a minimum width. ✅ (It wasn't fully fixed until prompt 21.)

**18.** "why the liner of these are different? do you actually follow the design rules?"
- The Primary vs Secondary border difference is in the spec. A full audit then found 9 real rule breaks (an off-palette color, off-rhythm gaps, a 50% radius, shadows, off-scale type, Info Blue misuse, a price without its restaurant, Orders hidden behind ☰, missing pressed states). All fixed. ✅

**19.** "/Users/marie/Downloads/Fonts_Package_….zip and upload this to the github. this is the font you should use for design"
- The file says "© McDonald's Corporation. All rights reserved", and it had only Speedee **Bold**. ✋ Not uploaded.
- **Decision (Marie): "Use it only when installed."** Installed on Marie's Mac. The site uses Speedee where it's installed and Inter otherwise. `.gitignore` blocks font files.

**20.** "why there's only pick up choice, it should have a "delivery " choice"
- Added **Delivery**: address, restaurant, a $2.99 fee shown in the bag before checkout, drop-off notes, and delivery on orders and receipts. ✅

**21.** "why the bar stuff is still shifting when i choose"pick up" or "delivery"
- Measured every header state: items moved up to 250px. Gave every header slot a fixed width and reserved the scrollbar space. Positions are now identical in 10 states at 7 widths. 🔁 ✅

**22.** "delete the line up the button"
- Removed the divider above the bag's Checkout button. ✅

**23.** "and i think the line of the top bar is kinda grey, not black"
- Measured the real site's line: #D6D6D6. Added **Divider #D6D6D6** to the spec palette and used it for every divider. ✅

**24.** "wait, all the line should be grey,right? and not that thick"
- Every line was already 1px. Explained the 3:1 contrast rule for button outlines.
- **Decision (Marie): "Muted grey"** (#7C7C7C) outlines on buttons, steppers and inputs; dark Ink only on selected options. Spec updated. ✅

**25.** "and also change the spec when you change them( like the fonts and liner)"
- Brought `docs/01-design-spec.md` and `docs/03-website.md` in line with the site. Since then, every design change updates the spec in the same commit. ✅

**26.** "why so little space? find a better space" (+ checkout, menu screenshots)
- Checkout titles had no space under them. Menu category titles sat closer to the section above than to their own products, because the photos have empty space above the food. Measured all 33 photos and trimmed each category's frame; it's now 60px between sections and 23px from title to food. ✅

**27.** "when there's nothing in the bag, this space seems"
- Bag button: fixed width with centered contents, so an empty bag has no gap. ✅

**28.** "and the font here should be these according to the original web"
**29.** "IT SHOULd be like this"
- Compared against the real site: size and spacing matched; only the typeface differed. Unselected categories need **Speedee Regular**, which wasn't installed. ✋ Asked for the file.

**30.** "bbut the thin font and thick font should be the same font … can you get that?"
- ✋ Didn't download McDonald's licensed font from their website. Offered to keep one family with Inter in the meantime. Marie wanted to clarify first.

**31.** "/Users/marie/Downloads/Fonts_Package_…/Speedee-Regular.otf i got the regular"
- Installed it. All text is now Speedee (Regular + Bold): one family, like mcdonalds.com. Spec updated. ✅

**32.** "for the products, it should be the name of the product in bold, price should be regulat"
- Menu cards: name Bold, price Regular, 6px apart. Totals stay Bold. Spec rule changed to match. ✅

**33.** "maybe you should push the file of fonts in github"
- ✋ Not uploaded: a public repo would make McDonald's licensed font downloadable by anyone, and a takedown could disable the whole site.
- **Decision (Marie):** Speedee should show for "any one who has access to the link of github".
- **Offered instead:** screenshots and a video of the site in Speedee in the README, plus a note explaining the font. Not decided yet.

**34.** "record all the propmpt and what you did and what decision i made. what we keep and what we change. make a file in website called"prompt" and one file for "process" (put all the process here, you can use before after pics)"
- This file, plus [process.md](process.md) with before/after pictures taken from each earlier version in the git history. ✅

**35.** "new figma desgin spec, update the pic in github" (+ new Design Spec frame)
- Replaced `assets/01-design-spec.png` with the new Figma export, which now includes the Divider color, the Lines table, Muted outlines, the Speedee note, 60px section spacing and the new components. ✅

**36.** "maybe add a readme for website. keep it core and simple"
- Added `website/README.md`: what it is, the live link, what you can do, the spec it's built on, the font note, and the files. ✅

**37.** "A redesign of the mcdonalds.com breakfast menu that lets you order on the website, with the same bag as the app. it should be “The McDonald's website only lets you browse the menu, and the app hides your bag, past orders and what you actually paid. So I redesigned both: …” something like this, redesign the cart nd reciept and make people can order online using laptop"
- Rewrote the website README intro around the problem and the fix (ordering on a laptop, a synced cart, receipts), using Marie's wording, with "we" because the app side is Xinyu's. ✅
