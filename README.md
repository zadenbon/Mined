# Mined
A lighter, faster fork of [Hazy](https://github.com/Astromations/Hazy) by [Astromations](https://github.com/Astromations). Same translucent glass look, without the CPU/GPU cost. Background blur and Canvas video are stripped out, and the UI is decluttered (no home page recommendations, no now-playing sidebar extras).
Hazy is itself based on [DynamicDefault](https://github.com/JulienMaille/spicetify-dynamic-theme) and [Bloom](https://github.com/nimsandu/spicetify-bloom).
## What's different from Hazy
- Removed background blur (`filter: blur()`) was the single biggest CPU/GPU cost
- Removed `backdrop-filter` blur on panels
- Disabled Canvas (looping video backgrounds)
- Hidden home page recommendations and now-playing sidebar clutter
- Noticeably less stuttering while scrolling large playlists
## Preview
**Custom Backgrounds**
![demo-base](./hazy_home.png)
![demo-base](./hazy_lyrics.png)
![demo-base](./hazy_play.png)
**Set Background To Album Art**
![demo-base](./custom_bg.png)

---

### ⬇️ Windows Installation ⬇️
Open **PowerShell** and run:

```powershell
iwr -useb https://raw.githubusercontent.com/zadenbon/Mined/main/install.ps1 | iex
```
---
### 📃 Manual Installation 📃
Download the repo and put `user.css`, `theme.js`, and `color.ini` into a new folder named `Mined`, and place this folder into your `Themes` folder in `.spicetify`. 

Then run these commands to apply:

```powershell
spicetify config current_theme Mined
spicetify config inject_css 1 replace_colors 1 overwrite_assets 1 inject_theme_js 1
spicetify apply
```
---
### 🐧 Linux 
Clone the repo, symlink it into your Themes folder, then apply. This way, editing the files in your clone updates the theme directly.

```bash
git clone https://github.com ~/Mined
ln -s ~/Mined ~/.config/spicetify/Themes/Mined
spicetify config current_theme Mined
spicetify config inject_css 1 replace_colors 1 overwrite_assets 1 inject_theme_js 1
spicetify apply
```
---
## Credits
Built on top of [Hazy](https://github.com/Astromations/Hazy) by Astromations. All credit for the original design and structure goes to them.
