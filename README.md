# Praktika — onboarding &amp; paywall rebuild

**Live prototype → https://bterzic123.github.io/praktika-flow-rebuild/**

A clickable rebuild of Praktika's onboarding and paywall, re-sequenced for conversion.
Open it in a browser, tap through it, or use the chips under the phone to land on any stage
with the answers already filled in. The right-hand panel explains every screen; the second
tab is the ranked list of changes.

## What this is

**The art direction is Praktika's, not ours.** The blue, the lavender cards, the tutor
chat-bubble header, the segmented progress bar, the projection chart, the plan cards, the
reminder toggle, the benefit-tile carousel and the Quick Chat with its correction sheet are
all rebuilt from Praktika's own screens. **Only the sequence changed.**

19 screens, down from roughly 26 plus three system dialogs.

## What was kept

- **The Quick Chat.** Before paying, the user holds a mic, speaks Spanish, makes a mistake and
  gets a correction with an explanation. Most subscription onboardings promise value; this one
  delivers it. Untouched.
- **The projection chart** — rebuilt as a working control. Change the minutes and the headline,
  the curve, the plan card's Duration row and the practice-hours date all move together.
- **The plan card that already works** — the Duration / Goal / Focus payoff screen. Praktika
  already computes a real plan, which is why the personalization loop is the right skeleton here.
- Every question the flow asks, bar one (see the table).

## Ranked changes

| # | Priority | Change | What changed | Expected impact |
| :-- | :-- | :-- | :-- | :-- |
| 1 | Fix first | Offer paywall on close | Closing the paywall ends the flow today. Now the X opens a second screen offering the 3-month plan Praktika already sells for $19.99. | ARPU +10–15% |
| 2 | Fix first | Paywall names the goal | The paywall says "your personal AI tutor" one screen after a card that said Travel. It now says "your Travel Spanish plan". | CR +15–20% |
| 3 | High | Permission prompts moved | Tracking, notifications and the microphone are all requested before the paywall, the first on screen 2. They now run after it. | CR +10–15% |
| 4 | High | Rating prompt out of the loader | The App Store rating request fires in the middle of "we're creating your plan". It moves to after the purchase. | CR +8–12% |
| 5 | High | Real proof before the ask | 4.7 stars from 164K ratings and 30M+ learners appear nowhere in the flow. They now sit before the speaking test and beside the paywall button. | CR +10–15% |
| 6 | High | Free vs Premium comparison | The paywall lists no difference between free and paid. Four rows above the plans show what changes. | CR +10–20% |
| 7 | Medium | Saving shown in money | The annual plan says $8 a month and the 3-month plan says $12, with nothing connecting them. The annual card now says it saves $45 a year. | CR +5–15% |
| 8 | Medium | Best value badge | Neither plan is marked as recommended. The annual plan gets the badge. | ARPU +5–10% |
| 9 | Medium | Loader shows the answers | The loader counts to 100 and says nothing. It now names the goal, the level, the focus, the pace and the topics. | CR +10–15% |
| 10 | Medium | Name, age and gender merged | Three screens in a row each ask one short question. They are now one screen. | CR +5–10% |
| 11 | Medium | Accent question merged | The accent is asked on its own screen, then asked again by the tabs on the tutor screen two taps later. | CR +5–10% |
| 12 | Low | Four interstitials cut to two | "Awesome!", "Perfect!", "Great!" and "Let me introduce my friends" are four full screens that ask nothing. Two remain, and they now name what the user just chose. | CR +3–8% |

## Grounding

Every price, rating, quote and feature row comes from Praktika's own published material: the
live US App Store listing, praktika.ai, and the supplied in-app capture frames. Third-party
pricing blogs were not used, and no statistic, trial length or testimonial was invented. The
full source list — including the figures that were deliberately *not* used and why — is in the
**Sources &amp; grounding** modal in the prototype.

The offer paywall rests on a real SKU: **Praktika Premium 3 Month Promo, $19.99**, listed on
Praktika's own App Store page.

## Run it locally

```bash
python3 -m http.server 8952
```

Then open http://127.0.0.1:8952/

---

*Impact ranges are Adapty's expected effect from teardowns and A/B tests across subscription
apps — not measured lift for Praktika.*
