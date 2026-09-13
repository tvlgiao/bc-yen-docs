# The other page templates

Yen Theme ships four custom page layouts. The Lookbook is covered above; the other three
work the same way — create a web page under **Storefront → Web Pages**, then pick the
template from the dropdown on that page's edit screen.

All three share one thing worth knowing before you start: **what you type into the web
page body is not what appears**. Each template renders its own content, so the page you
create supplies the URL and the template choice and nothing else. This is the same
arrangement as the Lookbook, for the same reason — the layouts are designed, not free-form.

## About

Choose the **About** template. Most of the content lives in the theme's language file
rather than in theme settings: the headings, the story paragraphs, the value cards and the
labels under the statistics all come from keys beginning `about.`.

The four statistic **numbers** are the exception. `50K+`, `10K+`, `50+` and `4.8★` are
written into `templates/pages/custom/page/about.html` itself, not into the language file —
searching `lang/en.json` for them will not find them. They are placeholder figures and
none of them describes your store, so have your developer change them in the template
before the page goes live.

The store name is substituted automatically wherever it appears, so it stays correct if you
rename the store.

## FAQ

Choose the **FAQ** template. It renders thirteen questions grouped into five categories,
with a search box and category filter that appear once the page loads.

The questions and answers are language-file content, under keys beginning `faq.`. The
sample text describes a generic store — free shipping over a threshold, a thirty-day
return window, a list of accepted cards — and **none of it is true of your store until you
change it**. Read through it before the page goes live.

Two things follow from the content living in the language file:

- the page is translated into all twenty languages the theme ships, so a shopper on a
  non-English storefront reads the FAQ in their own language
- the same text feeds the page's structured data, so a search engine is told exactly what
  a visitor sees — change one and the other follows

## Editing language-file content

The About and FAQ pages both take their words from `lang/`, and each language has its own
complete copy: `lang/en.json`, `lang/de.json`, `lang/ja.json` and so on. Editing
`lang/en.json` changes the English storefront and nothing else.

If your store serves more than one language, every locale you have enabled needs the same
edit. The theme ships translations of the sample text, so those pages read correctly out of
the box — but the moment you replace the samples with your own policies, the other
languages still describe the samples until they are updated too.

## Track Order

Choose the **Track Order** template. It tells a shopper where their orders are and what the
five order stages mean.

It deliberately does **not** offer an order-number lookup form. BigCommerce provides no
storefront endpoint a theme can query for a guest's order, so a form asking for an order
number and an email could not do anything with them. What the page offers instead is what
actually works:

- a signed-in shopper gets a link to their order history, where every order carries its
  status and, once it ships, its tracking link
- a guest is told that a tracking link is emailed when the order ships, and is offered
  sign-in — or, if they checked out as a guest, a password reset using the address they
  gave at checkout, which is BigCommerce's own route to an order history
