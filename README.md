# AI video model credit costs

Credits charged per clip in Twistavo AI Studio, checked on 2026-11-21.

The table lists 26 AI video models, grouped by model family, with the number of credits one 5-second clip and one 10-second clip cost in [Twistavo](https://twistavo.com) AI Studio, and the dollar value of those credits at the $3.99 entry price.

- Source page: https://twistavo.com/pricing/clip-cost
- Price of every model (image and video): https://twistavo.com/pricing/models

## Files

| File | Content |
|---|---|
| `data/clip-costs.csv` | One row per model and clip length (52 rows) |
| `data/clip-costs.json` | Same rows, with the source URL and check date |

## Columns

| Column | Meaning |
|---|---|
| `model_family` | Model family, as grouped on the source page (Grok, Seedance, Kling, Wan, MiniMax, Gemini, Happy Horse Video, FLUX) |
| `model` | Model name as shown in AI Studio |
| `clip_length_seconds` | Clip length: 5 or 10 seconds |
| `resolution` | Resolution of the quote: the model's default resolution. `Default output` means the page shows no fixed resolution for that model |
| `sound` | `on` when the model offers sound and the quote includes it; `not offered` when the source page shows "—" |
| `credits` | Credits charged for one clip |
| `usd_at_entry_price` | Dollar value of those credits at the $3.99 entry price (Mini plan, 180 credits, so one credit costs $0.0222) |
| `checked_on` | Date the source page was read |

## How to read it

Compare the `credits` column across models for the same `clip_length_seconds`. Credits are the unit AI Studio charges; the dollar column is only a conversion at the entry price. At the Agency rate ($499 for 47,000 credits a month), one credit costs $0.0106, so the dollar cost of the same clip is lower.

Example: a 5-second clip with Grok Imagine Video 1.5 Lite costs 43 credits ($0.95 at the entry price); the same clip with Seedance 2.5 costs 301 credits ($6.67).

## Methodology

From the source page:

- Each price is the live AI Studio quote of that exact request: the model's default resolution, sound on when the model offers it, no reference media.
- At start AI Studio holds the quote plus 15 %; the hold is returned when the clip completes.
- A failed or refused generation returns its credits to your balance.
- The price appears before each run, and you confirm it.

What changes the cost: a higher resolution costs more credits on most models; longer clips cost more; turning sound on can raise the price on models that offer it; start frames, reference images or source videos can change the quote.

Prices change when models change. The source page is the reference; this repository is a dated snapshot.

## Licence

[CC BY 4.0](LICENSE). Credit: "Twistavo, AI video cost per clip, https://twistavo.com/pricing/clip-cost".
