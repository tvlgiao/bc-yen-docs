# The Theme Editor, section by section

The editor is organised into nine sections. One of them, **Yen Theme**, holds everything
about how the storefront looks. Another, **Lookbook**, configures the shoppable-scenes
page. The remaining seven are `i18n.*` sections holding storefront wording, which
BigCommerce fills from the theme's language files — most stores never open them.

## Dark Mode

Yen Theme has a real dark mode, not an inverted filter. Both palettes are designed.

| Setting | Effect |
| --- | --- |
| **Theme Mode** | `System` follows the visitor's operating system preference, `Light` and `Dark` force one. Default: `System`. |
| **Dark Toggle** | Shows a toggle button in the header so visitors can override whatever the default was. |

A visitor's choice is remembered in their browser and survives page loads. The theme sets
the mode before the page paints, so there is no flash of the wrong palette on load.

## Colors

Five colours drive the whole storefront. Every component derives from them, so you do not
need to restyle pieces individually.

| Setting | Used for |
| --- | --- |
| **Accent** | Highlights, sale flags, active states |
| **Primary** | Buttons, links, anything the shopper is meant to click |
| **Heading** | Headings |
| **Text** | Body copy |
| **Muted** | Secondary copy, captions, metadata |

Each variation ships a palette that meets WCAG AA contrast in both light and dark mode. If
you change these values, check the result in both modes — a colour that reads well on white
often fails on the dark surface.

## Layout

| Setting | Options | Default |
| --- | --- | --- |
| **Background** | colour | — |
| **Surface** | colour used for cards and panels | — |
| **Border** | colour | — |
| **Max Width** | 1200px, 1400px, 1600px | 1400px |
| **Border Radius** | 0px, 8px, 14px, 20px | 14px |

Border Radius applies globally — buttons, cards, inputs, images. `0px` gives a hard-edged
look; `20px` is soft and rounded.

## Typography

Yen Theme uses **Plus Jakarta Sans** by default: weight 400 for body copy, 700 for
headings. Change fonts under the standard Stencil **Typography** controls; the theme's
heading scale (48 / 32 / 22 / 18 / 16 / 14 px) adapts to whichever family you pick.

## Announcement bar

Up to three rotating messages across the top of every page. Leave a message empty to skip
it; leave all three empty to hide the bar.

## Mega menu

Two promotional slots inside the navigation dropdowns, each an image plus a link: one under
**Categories**, one under **Shop**. There is also a banner image and text for the
All Categories panel.

## Homepage

| Block | Controls |
| --- | --- |
| **Trust badges** | On/off, plus a title and a line of text for each of three badges |
| **Promo banner** | On/off, one wide banner image, three supporting images, and an option to repeat the trust badges beneath |
| **Flash sale** | On/off, source (Best Sellers, Featured, or New Arrivals), title, text, and an end date that drives the countdown |
| **Reviews** | On/off, an aggregate score and count, and three named quotes |
| **Newsletter** | On/off, title and text |
| **Brand story** | On/off |
| **Press bar** | On/off, a title, and five logo-plus-link slots |

## Product pages

| Setting | Effect |
| --- | --- |
| **Sticky ATC Bar** | Keeps an add-to-cart bar visible as the shopper scrolls past the buy box |
| **Q&A Tab** | Adds a questions tab to the product tabs |

## Cart

| Setting | Effect |
| --- | --- |
| **Free Shipping ($)** | The threshold the shipping progress bar counts toward: 25, 50, 75, 100, 150, or 200 |
| **Shipping Bar** | Shows the progress bar |
| **Cross-sell** | Shows related products in the cart |
| **Trust Badges** | Shows the badges in the cart |
| **Recently Viewed** | Shows a recently-viewed strip, with a configurable item count |

Set the **Free Shipping** threshold to match the free-shipping rule you configured in
**Settings → Shipping**. The theme does not read your shipping rules; it only draws the bar.
