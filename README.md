# Ameck House Catalogues

Live at **https://catalogue.ameckhouse.com** (served by GitHub Pages from this repo, `main` branch).

Read this before adding products or editing anything.

## What is in here

| Folder | Catalogue | Serial prefix |
| --- | --- | --- |
| `kids/` | Kids | KD |
| `footwear/` | Footwear | FW |
| `bags/` | Handbags | BG |
| `home-decor/` | Home Decor | HD |
| `home-improvement-utility/` | Home Improvement and Utility | HD |
| `eyewear/` | Eyewear | SG |
| `design-furnishing-studio/` | Design and Furnishing Studio | DS |

`index.html` at the root is the landing page that links to all seven. `CNAME` holds the custom domain, do not touch it.

Each catalogue is one self contained `index.html`: HTML, CSS and JavaScript all in that single file.

## Adding a product

1. Open the `index.html` inside the right category folder.
2. Find the `PRODUCTS` list near the bottom of the file.
3. Copy the entry above and edit it. Keep the fields the same as its neighbours, they are not identical across catalogues.
4. Give it the next free serial for that catalogue, for example KD-079.
5. Put the photo links in the `images` list. Photos are uploaded to Shopify Files, we do not create Shopify products any more.
6. Commit. The live site updates in a minute or two.

## Things that happen automatically, do not do them by hand

- **The Shipping and Pricing note.** Every product shows it on its own. Do not paste it into the description, it would appear twice. The wording is deliberately generic, "This product can be ...", so it works for every catalogue. Please do not change it to a category name.
- **Photo thumbnails and swiping.** Both are built from the `images` list. Add photos there the normal way and they work.
- **There is no limit on how many photos a product can have.** Anything over five used to break the product page on mobile. That is fixed.

Optional: a product can carry its own `shippingNote` to override the default note. The furniture catalogue uses this because furniture ships by sea only.

## Rules

- **Do not change the shared look and feel without asking Anshuka.** Colours, fonts, spacing, layout, the product popup, the category tabs. Adding a product must not require any CSS change.
- **The seven catalogues do not share code.** There are three different product popup structures in this repo. If a change is meant to apply everywhere, it has to be made in all seven files and checked in all seven. Several past bugs came from a fix that only reached some pages.
- **Check on a real phone before calling it done.** Most of the bugs we have had looked perfectly fine on a desktop browser.

## Known quirks

- `home-decor` and `home-improvement-utility` both use the **HD** prefix, and HD-001 to HD-005 are the same five products listed in both catalogues. Edit a product in one and it will not change in the other. Worth cleaning up.
- GitHub Pages serves the old version for a minute or two after a commit. If a change looks missing, wait and hard refresh before assuming it failed.
- In the GitHub web editor, the "Commit changes..." button sometimes does nothing on the first click. Click it again.

