# Richard Osungu — editable portfolio

This is the unpacked version of your supplied portfolio. The page content, layout,
fonts, images, animations, links, CV and notebooks are preserved. No build step is required.

## Edit text
Open the corresponding `.dc.html` file in a text editor and search for the sentence
you want to change. Text is now readable HTML, not an encoded bundle.
`index.html` is the landing page; `Home.dc.html` is the same homepage at its existing URL.
Keep those two files in sync when changing the homepage.

## Edit images
Images are ordinary files in `assets/images/`. Find the `<img>` or `<image-slot>` in
the page and change its `src` to the replacement image path. Keep its dimensions,
style and crop settings to preserve the layout. Update `alt` text as appropriate.
`asset-map.json` records each original embedded asset and its extracted location.

## Design and behavior
Shared fonts and page styles live in `assets/css/`; fonts are in `assets/fonts/`.
The original inline styles are retained next to their elements for fidelity.
Page interactions are readable in the `text/x-dc` script at the bottom of each page.
`assets/vendor/` holds the original rendering libraries (including React and the
Claude DC runtime). Keep those libraries and their license comments intact.
`assets/js/` maps runtime dependencies to local files. No CDN is needed for those.
The small inline SVG textures are deliberately retained.

## Preview
Serve this folder with a local web server, for example `python -m http.server 8000`,
then visit http://localhost:8000/. A web server is recommended because the original
runtime uses browser loading features. No dependency installation or build is needed.

## GitHub Pages
These files can replace the existing published site files after review. Preserve
this folder structure and all `.dc.html` filenames so existing links keep working.
The published site uses these unpacked files.

## Next phase: visual editor
An editor has not been added yet. These readable pages and separate images provide
a foundation for one. A future editor should save content through an authenticated
workflow rather than placing GitHub credentials in public website code.

