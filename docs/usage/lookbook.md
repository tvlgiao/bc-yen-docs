# The Lookbook

The Lookbook is a shoppable page: a photographed scene with numbered dots over it, and a
strip of product cards beneath. Clicking a dot highlights its product.

## Creating the page

1. Create a web page in your control panel under **Storefront → Web Pages**.
2. On that page's edit screen, choose **Lookbook** from the template dropdown. The theme
   ships the template as a custom page layout, so it appears there once the theme is
   applied — there is nothing to upload separately.
3. Configure the content in **Theme Editor → Lookbook**.

The Lookbook is a single page. Its content lives in theme settings rather than on the web
page itself, so the page you create only supplies the URL and the template choice.

The page holds three blocks: a hero, **four looks**, and a "Shop by Room" grid.

## Configuring a look

All four looks take the same six fields. Using Look 1 as the example:

| Field | What to enter |
| --- | --- |
| **Look 1 Title** | The heading for the scene |
| **Look 1 Text** | A sentence or two beneath it |
| **Look 1 Image** | The scene photograph |
| **Look 1 IDs** | Product IDs, comma separated: `113, 115, 117` |
| **Look 1 View All URL** | Where "View all" links to — usually a category |
| **Look 1 Hotspots** | Dot positions, see below |

## The hero and the Shop by Room grid

The hero at the top of the page takes an eyebrow, a title, and a line of text.

Beneath the looks sits a **Shop by Room** grid: a title, a subtitle, and four tiles. Each
tile takes a label, a link, and an image. It is a plain navigation grid — no product IDs,
no hotspots.

## Product IDs

Enter them comma separated. Spaces do not matter, and a repeated ID is counted once.
Anything that is not a number is ignored, so a typo cannot break the page — it just drops
that entry.

**Only the first four IDs render as cards.** Extra IDs still count toward the
"View all N pieces" label, which is deliberate: it lets you show four pieces and tell the
shopper there are twelve.

Find a product's ID in the control panel under **Products → View**, in the ID column.

## Hotspots

Hotspots are the numbered dots on the scene. Enter them as `x,y` pairs separated by pipes:

```
30,40|65,25|50,80
```

Both numbers are percentages of the image, measured from the top-left corner. `30,40` sits
30% across and 40% down. Values outside 0–100 are pulled back to the edge, and a malformed
pair is skipped rather than breaking the page.

Dots are numbered in the order you list them, and each dot corresponds to the product in
the same position in **Look 1 IDs** — the first pair marks the first ID, and so on. List
the pairs in the same order as the products.

## What the Lookbook needs from your store

The Lookbook loads its product cards through your store's own Storefront GraphQL API, using
a token BigCommerce generates for each page render. There is nothing to configure and no
key to paste — it works on any store the theme is installed on.
