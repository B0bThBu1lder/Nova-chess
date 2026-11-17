NOVA CHESS — iPhone PWA

WHAT'S INCLUDED
- Responsive chessboard with legal move validation (chess.js)
- Stockfish 19 lite single-threaded WebAssembly engine, loaded on first analysis
- Approximate engine Elo limiter (Stockfish UCI_LimitStrength / UCI_Elo)
- Bullet and Normal thinking presets
- FEN position loading and copying
- Best-move arrow, evaluation, depth, and play-best-move control
- Saved preferences via localStorage
- Theme colour, board colour, arrow colour, highlight colour, panel opacity, arrow opacity
- PWA manifest and service worker app-shell cache
- Same-origin worker loader for iOS Safari compatibility

IMPORTANT iPHONE SETUP
A PWA must be served from HTTPS (or localhost) to install and use its service worker. An HTML file opened directly from Files is not an installable PWA and may block workers.

Quick deployment:
1. Upload the contents of this folder to a static HTTPS host (for example GitHub Pages, Cloudflare Pages, or Netlify).
2. Open the resulting HTTPS URL in Safari on iPhone.
3. Tap Share → Add to Home Screen.
4. Launch NOVA CHESS from the Home Screen.
5. Tap Analyse position. The Stockfish worker is downloaded from jsDelivr on first use; internet is required for that first load.

CHESS.COM LIMITATION
This is a separate analysis app. iOS does not allow it to inspect or draw over the native Chess.com app. Enter a position using the board or paste a FEN. It is intended for analysis and study, not live-game assistance.

ENGINE
Stockfish.js v19.0.1 lite single-threaded build is loaded by stockfish-loader.js from:
https://cdn.jsdelivr.net/npm/stockfish@19.0.1/bin/
The loader sets the WASM asset URL explicitly. The app starts the same-origin worker wrapper, which imports the Stockfish script and avoids Safari's cross-origin Worker constructor restriction.
Stockfish is GPL-3.0. chess.js is BSD-2-Clause.
