# USD Transaction Processing — HSBC & Macquarie (AUD Accounts)

<!-- tag: sources -->

How USD card spending and ATM withdrawals are processed when paying from an
**AUD-only** account at the traveller's two banks: **HSBC Australia** and
**Macquarie**. Scope: card purchases (in-store and online) and ATM cash in the
USA. Out of scope: international wire transfers, currency exchange before travel.

Date researched: 2026-06-12. All fees and rates are indicative; confirm against
each bank's current fees schedule and your specific account terms before the trip.

## How an AUD-Account USD Transaction Works (Both Banks)

1. You pay in USD (card tap/swipe/online, or ATM withdrawal).
2. The conversion USD → AUD happens at a daily FX rate. For **Macquarie** this is
   the **Mastercard** scheme rate (close to mid-market). For **HSBC Everyday
   Global**, because USD is a supported currency, HSBC uses its **own** rate, not
   the Visa rate (the Visa rate applies only to currencies HSBC doesn't support).
3. Your AUD balance is debited the converted amount, **plus** any bank foreign /
   international transaction fee (see per-bank tables below).
4. The USD merchant's bank or the ATM operator may add **their own** surcharge —
   neither HSBC nor Macquarie controls this.

**Always choose to be charged in USD (local currency), never AUD.** If a terminal
or ATM offers "pay in AUD" (Dynamic Currency Conversion), it uses the merchant's
own poor rate with a wide spread — decline it so your bank/card scheme does the
conversion instead.

## Transaction Lifecycle & When the Rate Locks (Mastercard)

A card transaction has two stages:

1. **Authorization** — at the point of sale, the merchant gets approval and a
   temporary hold is placed. For a foreign-currency purchase, Mastercard computes
   the AUD amount here.
2. **Clearing / settlement** — the merchant submits the transaction for processing,
   usually within 1–3 days (longer for some hotels, car hire, and pre-auths). The
   final amount posts to your account.

**Common worry: "does Mastercard pick the worst rate during the settlement
window?" — No.** This is a myth. The facts:

- Mastercard publishes **one single rate per currency pair per day**, derived from
  wholesale market rates (and government-mandated rates where they apply). It does
  **not** scan a window and select the least favourable rate.
- Since 11 Aug 2020, the rate applied is the rate **in effect on the date your bank
  authorizes the transaction** — i.e. **locked at the point of sale**, in your
  favour. Market moves between purchase and settlement do **not** change it.
- **Only exception:** if a merchant submits the transaction for processing **9 or
  more days** after authorization, the rate at the **processing date** is used
  instead. This can affect delayed-capture merchants (some hotels, car rental
  final bills, deposits). That rate is still the single daily market rate — better
  or worse purely with the market, not cherry-picked.
- The **pending hold** you see in-app may differ slightly from the final posted
  amount. That is the authorization estimate vs the final cleared figure, not
  Mastercard re-pricing against you.

**Net:** for normal purchases and ATM withdrawals the fixed rate is favourable —
it is locked when you tap, at a single transparent daily rate. Residual timing risk
exists only for transactions captured 9+ days late, and there the exposure is
ordinary market movement, not an adverse rate selection.

(Visa works similarly but, unlike Mastercard, traditionally applies the rate on the
**processing/settlement** date rather than authorization. This is moot for your
HSBC card, which converts USD at HSBC's own rate, not the Visa rate.)

### Why the HSBC online quote moves but the Mastercard quote doesn't

The two banks expose two different *kinds* of rate, which is why one ticks every
few seconds and the other sits still:

| | Mastercard (Macquarie) | HSBC Everyday Global (USD) |
| --- | --- | --- |
| Rate type | A **single benchmark rate per currency pair**, set **once per business day** (≈2:05 pm US Central, so ≈early morning Sydney). Holds steady the rest of the day and over weekends/US holidays | A **live, tradeable market quote** streamed in real time — updates every few seconds |
| Rate at your transaction | That day's Mastercard rate, **locked at authorization** | The **live HSBC rate at the moment of conversion**, or the rate you **locked** if you pre-loaded USD |
| Can you preview your exact rate? | **Yes** — the Mastercard currency converter shows the rate you'll actually get | Only by locking it in; otherwise it's whatever the feed reads when the transaction posts |

**Key point:** the Mastercard rate is **not** secretly dynamic — it genuinely
changes only once a day, and the converter is an accurate preview of your
transaction rate. HSBC's rate is genuinely intraday-dynamic and is sampled at the
moment of conversion (or pre-lock). Neither is "hiding" a rate from you.

### Does the daily fix carry a hidden margin against you? (90-day view)

Concern: a once-a-day fixed rate must be padded with a safety buffer (unfavourable
to the cardholder) to protect the setter against the day's market moves.

There is a real kernel here — **any** rate held fixed over time exposes the quoter
to FX risk, and a rational quoter pads for it. But the buffer scales with **how
long** the rate is held and **who carries the risk**, and for Mastercard both are
small:

- The fix lasts only **~1 day** and resets near the wholesale market each day. A
  1-day hold needs a tiny buffer, unlike an airport bureau or prepaid travel card
  that locks a rate for days/weeks (those *do* pad heavily).
- Mastercard isn't warehousing large unhedged retail-card FX exposure; settlement
  between banks happens at the set rate, derived from current interbank rates.
- The fix hits you as **symmetric timing noise, not a one-way margin**: your
  transaction uses a snapshot up to ~24h old, which is sometimes better and
  sometimes worse than the live rate — averaging ≈ zero over many transactions.
- The only *systematic* cost is Mastercard's small markup over interbank, widely
  ~≤0.5% for a liquid pair like AUD/USD — separate from the daily-fix mechanism.

**90-day empirical view (mid-Mar – mid-Jun 2026).** Note: Mastercard does not
publish a downloadable history of its own AUD/USD rate, so this rests on (a) the
AUD/USD market series, which is real data, and (b) the documented near-interbank
nature of the Mastercard rate — not on a fabricated Mastercard daily table.

- AUD/USD traded ~**0.698 – 0.726** (peak 0.7259 on 13 May; dipped to ~0.6986 on
  11 Jun). ~4% peak-to-trough over the quarter, but **daily** moves were modest:
  largest single 24h move ~**0.57%** (5 Jun), typical days ~0.2–0.4%.
- So the timing variance a 1-day fix injected was ~**±0.2–0.5% on a typical day**
  (rarely ~0.6%), and symmetric.
- That is dwarfed by the **~2% structural margin** baked into HSBC's live rate. A
  live rate marked up 2% is worse on *every* day than a near-interbank rate that is
  a few hours stale.

**Verdict:** the daily fix was **good for you, not bad** over the period. It is not
a hidden anti-customer buffer — near interbank, small symmetric timing wobble, and
~1.5–2% cheaper than HSBC's marked-up live rate essentially every day. The option
that *feels* safer (HSBC's ticking live quote) is the structurally costlier one.

**Verify it yourself** (since the exact Mastercard series isn't downloadable): on a
few days, at the same moment, compare the Mastercard converter AUD→USD rate against
xe.com / Wise mid-market — expect a gap well under ~0.5%. Do the same with HSBC's
quote to see its ~2% gap.

### Empirical check with one month of actual Mastercard rates (17 May – 10 Jun 2026)

Traveller supplied the Mastercard daily fixed rate as **AUD paid per 100 USD** for
25 consecutive days. The data confirms the analysis above.

| Metric | Value |
| --- | --- |
| Cheapest USD (best for buyer) | **139.78 AUD / 100 USD** on 26 May (implied AUD/USD 0.7154) |
| Dearest USD | **142.94** on 10 Jun (implied AUD/USD 0.6996) |
| Net move over the month | USD **~+2.0%** more expensive (AUD weakened ~0.714 → ~0.700) |
| Peak-to-trough range | **2.26%** — driven by market, not the rate mechanism |
| Typical daily move | **~0.34%** business-day to business-day |
| Largest single-day move | **~0.90%** (4→5 Jun, AUD fell) — symmetric (e.g. −0.71% on 28→29 May) |
| Markup vs mid-market | **~0.3–0.5% (avg ~0.4%)** on dates with a mid-market anchor (31 May, 1/2/4 Jun) |

Confirming signatures in the data:
- **Weekend holds**: three identical values on Fri–Sun (141.72 on 5–7 Jun; 140.55
  on 22–24 May; 139.94 on 29–31 May) — the fingerprint of a once-a-day fix.
- **Symmetric wobble, not a one-way buffer**: daily moves go down for the buyer
  about as often as up; no systematic anti-customer drift.

**Conclusion from real data:** the Mastercard daily fix carried only a ~0.4%
systematic margin and small symmetric daily noise. It beat HSBC Everyday Global's
~2% margin by roughly 1.5% on every day in the sample. The ~2.3% swing visible in
the month was AUD weakness (market), which HSBC would have tracked too — plus its
~2% load. The daily fix was favourable, not unfavourable.

## Macquarie — Transaction Account (debit Mastercard)

| Item | Detail |
| --- | --- |
| International / foreign transaction fee | **$0** (Macquarie charges nothing on overseas purchases, in-store or online) |
| Overseas ATM withdrawal fee (Macquarie side) | **$0** |
| FX rate used | **Mastercard FX rate** (scheme wholesale rate; small Mastercard margin, no extra Macquarie margin) |
| Third-party charges | Foreign ATM operators / merchants may still add their own fee |

**Bottom line:** Macquarie's transaction account is effectively fee-free for USD
spending and ATM cash — you pay only the Mastercard conversion rate plus any
foreign ATM operator's own surcharge.

## HSBC Australia — Everyday Global (confirmed account)

Traveller confirmed (2026-06-12) the HSBC card is linked to the **Everyday Global**
account. This is the fee-free multi-currency Visa Debit product.

### HSBC Everyday Global Account (multi-currency Visa Debit)

| Item | Detail |
| --- | --- |
| International / foreign transaction fee | **$0** |
| Overseas ATM withdrawal fee (HSBC side) | **$0** |
| FX rate used for USD | **HSBC exchange rate** — *not* the Visa rate. USD is a supported currency, so HSBC converts at its own rate whether you pre-load USD or convert live at point of sale |
| FX rate for *non*-supported currencies | Visa scheme rate (only applies to currencies HSBC doesn't support, e.g. Thai baht) |
| HSBC rate margin (USD) | **~2%** over mid-market (user-reported ~2.1%; HSBC markets it as "competitive" — confirm with a live quote) |
| Pre-load vs point-of-sale | **Same HSBC rate either way.** Pre-loading does not lower the margin — it only locks the rate earlier (a hedging tool, not a saving) |
| Third-party charges | Foreign ATM operators / merchants may still add their own fee |

**Bottom line:** fee-free like Macquarie, but the USD conversion uses HSBC's own
rate (~2% spread), which is wider than the Mastercard scheme rate. See FX margin
comparison below.

## FX Margin Comparison — the real cost on a fee-free card

With both cards at $0 fees, the only remaining cost is the **FX margin** (how far
the conversion rate sits above the true mid-market/interbank rate). All figures
indicative — confirm with a live quote on the day.

| Path | Rate used | Typical margin over mid-market |
| --- | --- | --- |
| Macquarie debit Mastercard | Mastercard scheme rate | **~0.2–0.6%** (tight) |
| HSBC Everyday Global — USD spend or pre-load | **HSBC rate** | **~2%** (user-reported ~2.1%) |
| HSBC Everyday Global — non-supported currency | Visa scheme rate | ~0.5–1% |

The Visa and Mastercard **scheme** rates track the mid-market rate closely (well
under 1%). HSBC's **own** rate for its supported currencies (incl. USD) carries a
wider spread (~2% in user tests). So for USD, the Macquarie Mastercard rate is the
most competitive option held.

## Should you pre-buy USD via HSBC FX, or convert at point of sale?

- **Pre-converting AUD→USD inside the Everyday Global account uses the same HSBC
  rate as a live point-of-sale conversion.** Pre-loading does **not** reduce the
  margin — it only locks the rate earlier. It is a **hedging tool, not a saving**:
  worth it only if you want to lock now because you expect the AUD to fall before
  the trip. If the AUD rises, you've locked a worse rate.
- **Neither HSBC path beats the card-scheme rate.** Pre-buying USD via HSBC FX
  locks in HSBC's ~2% spread, which is wider than the ~0.2–0.6% Mastercard rate you
  get by simply spending on the Macquarie card in USD.
- **Conclusion:** don't pre-buy USD to save money. For lowest cost, spend on the
  **Macquarie Mastercard** in USD and let Mastercard convert. Only pre-load USD on
  HSBC if you specifically want to hedge against AUD weakness.

## Comparison Summary

| Card / account | FX rate | Foreign txn fee | Overseas ATM fee (bank) | Verdict for USA |
| --- | --- | --- | --- | --- |
| Macquarie Transaction Account | Mastercard (~0.2–0.6% margin) | $0 | $0 | **Best — primary card** |
| HSBC Everyday Global | HSBC rate for USD (~2% margin) | $0 | $0 | Good — Visa backup; rate wider than Macquarie |

## Recommendations

1. **Primary card for the US trip: Macquarie debit Mastercard** — $0 fees and the
   tightest FX margin. Default for purchases and ATM cash.
2. **HSBC Everyday Global = fee-free Visa backup.** Use it where a merchant favours
   Visa or if the Macquarie card is blocked — but note its USD rate is ~2%, wider
   than Macquarie's, so it is the second choice on cost.
3. **Do not pre-buy USD via HSBC FX to save money** — same ~2% HSBC rate as live
   conversion, and wider than the Mastercard rate. Pre-load only to hedge AUD risk.
4. Carry **two cards on different networks** (Mastercard + Visa) so a network
   outage or a single-card block never leaves the family without payment.
5. At every US terminal/ATM, **decline "pay in AUD" (DCC)** — always pay in USD.
6. Prefer fewer, larger ATM withdrawals to minimise per-withdrawal **operator**
   surcharges (common US ATM surcharge is ~USD $3–5, set by the ATM, not your bank).
7. Notify both banks of US travel dates (or check in-app travel settings) to avoid
   fraud blocks on USD transactions.

## To Confirm (live check before travel)

- HSBC: get a **live Everyday Global USD quote** and compare against mid-market to
  confirm the current margin (user reports ~2%, HSBC markets it as competitive).
- Macquarie: re-confirm $0 international transaction fee still current at travel
  date (policy as of Jan 2026), and compare a live Mastercard rate vs mid-market.
- Both: current overseas ATM fee, daily ATM/withdrawal and contactless limits.

## Sources

- [Macquarie — Overseas charges and exchange rates](https://www.macquarie.com.au/help/personal/international-and-travel/travelling-overseas/overseas-charges-and-exchange-rates.html)
- [Macquarie — Transaction account](https://www.macquarie.com.au/everyday-banking/transaction-account.html)
- [Wise — Using your Macquarie debit card overseas](https://wise.com/au/blog/macquarie-debit-card-overseas)
- [HSBC AU — Everyday Global Account](https://www.hsbc.com.au/accounts/products/everyday-global/)
- [HSBC AU — Everyday Global FAQ](https://www.hsbc.com.au/accounts/products/everyday-global/faq/)
- [HSBC AU — Visa Debit Card](https://www.hsbc.com.au/accounts/products/visa-debit/)
- [HSBC AU — Essential foreign exchange & travel tips](https://www.hsbc.com.au/accounts/essential-foreign-exchange-travel-tips/)
- [Wise — Using your HSBC AU debit card overseas](https://wise.com/au/blog/hsbc-au-debit-card-overseas)
- [Mastercard — Currency conversion calculator](https://www.mastercard.com/global/en/personal/get-support/convert-currency.html)
- [Wise — What is the Mastercard exchange rate?](https://wise.com/gb/blog/mastercard-exchange-rate)
- [exchangerates.org.uk — AUD/USD spot history 2026](https://www.exchangerates.org.uk/AUD-USD-spot-exchange-rates-history-2026.html)
