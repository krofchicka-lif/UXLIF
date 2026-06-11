# Love it Forward (LIF) × Moon Juice — Surface System

**Give Good. Feel Good. Love it Forward.**

A complete, clickable design canvas for **Love it Forward (LIF)** — customer-funded growth infrastructure — shown end to end inside a real merchant (Moon Juice). One chain, every surface it touches, both viewports.

> Love it Forward (LIF) turns the most human moment in commerce — *"you have to try this"* — into a measurable growth channel. Someone chooses you. You discover who. You pass it on. Every continuation is a new purchase, never a forward.

---

## View it

Open **`index.html`** in any modern browser, or serve the folder and visit the root. No build step — everything runs client-side (React + Babel via CDN).

- **GitHub Pages:** push this repo, enable Pages on the default branch, and the canvas loads at your Pages URL (`index.html` is the entry point).
- **Local:** any static server works, e.g. `npx serve` then open the printed URL. Opening `index.html` directly via `file://` also works.

The canvas is **pan + zoom**. Scroll to pan, ⌘/Ctrl + scroll (or pinch) to zoom. Click any artboard label to open it fullscreen; press Esc to exit. Two artboards are fully interactive — the **giver flow** (click *Love it Forward*) and the **reveal flow** (tap *Find out who*).

---

## The chain

`Amy buys → Amy sends a LIF → Jody is chosen → Jody reveals and redeems → Jody continues to Rachel`

Amy is the originator. She does not forward anything — she *chooses* people. When Jody continues the chain, she makes a brand-new purchase for Rachel. That is the entire business model:

> There is no forwarding. Every continuation is a new purchase. Every new purchase creates a new customer.

---

## What's in the canvas (62 artboards)

Every page ships as a pair: **M** (375px, iPhone) and **D** (1280px, browser). Mobile is primary except Pages 13, 16, and 17, where desktop leads.

| Section | Surfaces |
| --- | --- |
| **Overview** | Read-me cover, the chain, the two design systems |
| **01 · Amy buys** | Standard Moon Juice checkout, $43.50. No LIF on screen yet. |
| **02 · Amy gives** | Thank-you discovery → multi-recipient chooser → one payment → sent → updates opt-in (interactive) |
| **03 · Jody is invited** | Email 1, the mystery invite |
| **04 · Jody reveals** | Pre-reveal → "It was Amy." → the note → reaction capture → the experience invitation, plus expired (12E) (interactive) |
| **05 · Jody redeems & continues** | $0.00 + partial-cover checkouts, receiver thank-you, Jody buys a LIF for Rachel, the loop-back, the core principle |
| **06 · Tracking** | The Chain tree (Amy's private view) and Pulse (merchant dashboard) |
| **07 · Emails** | Invitation, giver confirmation, opened, revealed, reaction, used it, kept it going, didn't-move credit |
| **08 · Notifications** | Giver lock-screen stack + receiver SMS, with trigger maps |
| **09 · Additional surfaces** | lif.co landing page, product-page widget, merchant gift page |

### Trigger map (which surface fires which message)

| Surface | Fires |
| --- | --- |
| Page 04 completion | Giver confirmation immediately; Email 1 to each recipient (60s delay per person) |
| Page 08 (opened) | Email 2 to Amy |
| Page 09 (revealed) | Email 2.5 to Amy |
| Page 11 (reaction) | Email 3 to Amy — *only if a reaction is left* |
| Page 13 (redeemed) | Email 4 to Amy |
| Page 15 (continued) | Email 5 to Amy + Email 1 to Rachel |
| Day 7 (unclaimed) | Email 6 to Amy — credit returned |

---

## Multi-recipient

Multi-recipient is an **option, not a requirement.** The default flow is one recipient. A giver may choose to Love it Forward to more than one person in a single purchase. Each recipient is always individual, intentional, and personal — own name, note, and value. *Add Another Person* appears after the first is complete; cap is 8. This is personal selection at scale, not a bulk-send feature.

---

## Design system

Built on the **LIF Design System**.

- **Two backgrounds only:** Air (`#FDFCF8`) and Not Black (`#2F2B2B`). No cream, no warm paper.
- **Color:** Sol gold on Air for primary action; Poppy red and Blue Jean as accents. One pigment per surface.
- **Type:** Romana BT (serif display, the human moment), Graphik (sans, headlines + body), Apercu (UI chrome).
- **Shape language:** square edges everywhere, one pill CTA. Paper shadows, never glass.
- **Voice:** short. short. short. one long thought that explains why. No exclamation marks. No em dashes.
- **Two systems, never mixed:** Moon Juice storefront chrome for commerce surfaces; full LIF color for the brand moments.

Cast stays Amy → Jody → Rachel throughout so the flow reads like real people.

---

## File structure

```
index.html                      ← GitHub entry point (copy of the working canvas)
LIF Moon Juice Surfaces.html    ← working canvas (same content)
colors_and_type.css             ← LIF design tokens + base type
frames/design-canvas.jsx        ← pan/zoom canvas component
lib/brand.jsx                   ← shared primitives (logos, chrome, buttons)
surfaces/
  shopify.jsx                   ← checkout, order summary, two redemption scenarios
  thankyou.jsx                  ← giver thank-you, multi-recipient modals, sent states
  lifco-reveal.jsx              ← the mobile reveal flow
  lifco-track.jsx               ← Chain tree + Pulse dashboard (desktop)
  emails.jsx                    ← all eight emails
  notifications.jsx             ← lock screen + SMS
  viewports.jsx                 ← iPhone bezel, desktop reveal, mobile dashboards, landing/widget/gift
assets/                         ← LIF wordmark + marks, Moon Juice logo, reaction photos
fonts/                          ← Romana BT · Graphik · Apercu
image-slot.js                   ← drag-and-drop slot for the real product photo
```

To drop in the real SuperYou product photo, open the **PP-D** or **PP-M** artboard and drag an image onto the placeholder — it persists locally.

---

*This is a brand-aligned design artifact. Moon Juice is used as an illustrative host merchant.*
