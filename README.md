# Dreamscreen

Dreamy live wallpapers that you shape in the browser. Dark, grainy, glowing gradients that drift slowly and loop without a seam.

The whole site is one file, `index.html`. There is nothing to build or install.

## What it does

- **Gallery** – 23 wallpapers drawn live in the browser.
- **Studio** – change the effect, colors, speed, scale, intensity, grain and vignette, add your own image or a line of text, then download.
- **Downloads**
  - **Lively Wallpaper** – a ZIP that the free Windows app [Lively Wallpaper](https://github.com/rocksdanister/lively) imports when you drop it into its window. Colors, speed and the rest stay adjustable under *Customise*.
  - **Wallpaper Engine** – a web wallpaper package with the same settings as properties.
  - **Image** – PNG or JPG up to 4K, ultrawide, portrait and iPhone sizes.
  - **Loop video** – exactly one loop, so it repeats without a jump.
- **Show** – the wallpapers as a full-screen projection for a wall, a TV or a screen behind a band. They cross-fade every 30 s, 1 min or 5 min, or hold on one. The picture can move with music from three sources:
  - **Mic** – the sound in the room.
  - **Song** – a music file the page plays itself.
  - **Computer** – whatever the computer is playing, Spotify included. A browser cannot listen to one app by itself, so in the dialog choose **Entire screen** and switch on **Also share system audio**. A browser tab with its audio works too. Desktop Chrome and Edge only.

  Every drum hit punches the picture toward you, makes it flare, swings its colors, jolts it and throws the motion forward. **Tune** opens a small mixing desk for that: five faders (Zoom, Light, Color, Shake, Speed) with the presets **Soft**, **Hard** and **Wild**, the music's spectrum behind them, and below them the effect and the colors of the wallpaper on screen.

## Run it

Open `index.html` in a browser, or host it on GitHub Pages:

1. Create a public repository and upload `index.html`, `README.md` and `LICENSE`.
2. In the repository open **Settings → Pages**.
3. Under **Build and deployment** choose **Deploy from a branch**, pick the `main` branch and the `/ (root)` folder, and save.
4. After a minute or two the site is at `https://<your-user-name>.github.io/<repository-name>/`.

The page needs an internet connection for its two typefaces (Google Fonts) and for the ZIP library used by the Lively and Wallpaper Engine downloads (JSZip from cdnjs). Everything else runs offline.

## Good to know

- The wallpapers need WebGL. Without it the page shows plain gradients in each wallpaper's colors.
- **Mic** and **Computer** need a secure address (`https://`), which GitHub Pages provides, and the browser asks for permission. The sound is only analysed in the page; nothing is recorded or sent anywhere.
- High Tune settings flash. The flare and the color swing fire at most three times a second, and the show stays still for anyone whose system asks for reduced motion, but keep the faders low around people sensitive to flashing light.
- The beat detection was tuned on synthetic test tracks (house, hip-hop, drum and bass, a quiet mix, an ambient pad), not yet on a library of real songs.
- Everything is free at the moment. The store (prices, cart, locked downloads) is still in the code behind one switch: set `const FREE = true;` to `false` in `index.html`.
- The **Dreamscreen Player** download makes a `.dreamscreen` file for a player app that does not exist yet.
- The Lively package was built from Lively's documentation and source and checked in a test browser, not yet in Lively itself.

## License

All rights reserved. You may use the site and keep the wallpapers for yourself; you may not copy the code or redistribute or sell the wallpapers. See [LICENSE](LICENSE).
