# NOVA CHESS — iPhone PWA

A mobile-first chess practice and analysis app with a starfield interface and local Stockfish engine.

## Features
- Interactive legal chessboard with undo, reset and flip
- FEN import and copy
- Stockfish 19 lite single-threaded engine
- Approximate engine strength setting (1320–2850)
- Bullet and Normal search presets
- Saved preferences (ELO, depth, mode, highlight colour, opacity)
- Installable PWA shell for iPhone Safari

## Deploy
1. Open repository Settings → Pages.
2. Set the source to **GitHub Actions**.
3. The included workflow deploys automatically on pushes to main.
4. Open the URL shown under Settings → Pages or the successful Actions deployment.

## iPhone install
Open the HTTPS Pages URL in Safari → Share → Add to Home Screen.

## Engine and network
Stockfish 19.0.1 lite single-threaded WASM and chess.js 1.4.0 are loaded from pinned public CDNs. No ChatGPT API or hosted inference is used. An internet connection is needed to load the engine and chess.js on first use.

Stockfish.js is GPL-3.0: https://github.com/nmrugg/stockfish.js
chess.js is BSD-2-Clause: https://github.com/jhlywa/chess.js

## Scope
NOVA is a practice and analysis board. Positions are entered manually or through FEN. It does not inspect the Chess.com app, overlay another app, or provide move recommendations during live matches. The ELO control is an approximate engine-strength setting, not a calibrated human-rating guarantee.
