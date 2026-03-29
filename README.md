# Bond Risk Monitor

A live GitHub Pages dashboard for tracking sovereign bond-market risk across countries using the BondStats global yield feed.

## What this tool does

The Bond Risk Monitor uses currently available live JSON data to create a transparent country-level bond risk framework.

It shows:

- current 10-year government bond yields
- recent yield changes
- yield pressure
- recent move pressure
- combined risk score
- live risk signal by country

## Why this version is different

The previous BondStats Bond Risk Monitor page was more static and included simplified reference values and model assumptions.

This GitHub version is designed to work directly from the live BondStats JSON feed and update automatically.

It does not fabricate 2Y/10Y spread data or recession signals when those inputs are not available in the current live JSON structure.

## Risk model

Each country risk score is based on two live inputs:

- Yield pressure  
  Higher outright 10Y yields imply higher sovereign financing pressure and therefore a higher baseline risk signal.

- Move pressure  
  Positive recent yield changes imply tightening pressure and increase the risk signal.

### Score formula

- 65% current yield level
- 35% recent positive yield move

This creates a simple, transparent sovereign bond stress monitor.

## Live data source

The tool reads from:

`https://botapi33.github.io/bondstats-global-yields/global_yields.json`

## Files

- `index.html`
- `README.md`
- `.nojekyll`
