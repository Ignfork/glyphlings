# Glyphlings ($GLYPH)

Single-file static site: `index.html` (no build step, no folders).

## Deploy
- **Vercel:** drag the files in (or import the repo), framework "Other", no build command.
- **GitHub Pages:** put `index.html` at the repo root and enable Pages.

## Config
At the top of the second `<script>` in `index.html`:

```js
var CONFIG={xUrl:'https://x.com/Glyphlings',ca:'',buyUrl:'',chartUrl:'',perGlyphling:5000000,supply:1000000000,noGlyphlings:[]};
```

- `xUrl`: your X account. The "Get the CA on X" button and the X icon point here.
- `ca` (optional): the contract address is never shown on the page. If you fill it in, the Wallets section uses it to read real $GLYPH balances.
- `noGlyphlings`: after launch, paste the pump.fun bonding curve address and the PumpSwap pool address here so they never count as holders.
- Empty links show a "coming soon" message instead of a dead link.

## Starting state
Everything starts at zero: no glyphlings alive in the colony, no families, no paid hours, no log events. The hatching, quine check, kids lab, species rules and rebuild tool all work right away because they run in the browser.

## pump.fun numbers used
- Total supply 1,000,000,000, 6 decimals
- About 800M sold on the bonding curve, about 200M seed the PumpSwap pool at graduation (LP burned)
- 5M per glyphling = 0.5% of supply, so 200 glyphlings max
- Payouts: 50% of the pump.fun creator fees (SOL), hourly. The site doesn't quote a fee rate because pump.fun's fee tiers change.
