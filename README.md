# Snap-to-Rank

An interactive prototype of a feature concept: turning a "new photos detected" notification into a one-tap
deep link straight into ranking the right restaurant — instead of dropping the user at a generic search bar.

**Not affiliated with, built by, or endorsed by Beli.** This is an independent concept prototype made by a
Beli user/fan, shared publicly as a portfolio piece. All restaurant names and data in the demo are fictional
mock data — no real Beli data, users, or infrastructure are involved.

## Try it

Open `index.html` in any browser — no install, no build step, no dependencies. (If GitHub Pages is enabled
on this repo, there's also a live link in the "About" section of the repo page.)

Pick a scenario from the left panel to see how the flow handles it: a clean single match, a food-hall cluster
with multiple candidates, permissions being off, a stale photo, an already-ranked place, and more. Scroll down
to **"Automated scenario checks"** and hit **Run all tests** to see the underlying matching logic verified
against each scenario live in your browser.

## How it works, briefly

A photo's GPS coordinates (when available) are matched against nearby restaurants by distance, with a
confidence score based on how close the match is relative to the GPS accuracy radius. A single high-confidence
match deep-links straight to that restaurant. Multiple close candidates trigger a quick "which one?" picker
instead of guessing. Anything uncertain — no location data, no nearby match, a low-confidence read, a stale
photo — falls back to ordinary search, never a wrong forced guess.

## Stack

Vanilla HTML/CSS/JS, one file, zero dependencies. Built this way on purpose — anyone can open it, read it, or
run it without any setup.
