# bitsbeam.com

Company site for bitsbeam: UFO + cow hero, company, products, "why bitsbeam" and an about page.
Plain static HTML / CSS / JS — no build step, no dependencies.
The Cosmonats site lives next door in `../cosmonats.bitsbeam.com/` and shares `assets/application.css` +
`application.js` — keep both copies identical.

## Structure

```
/
├── index.html            # hero (UFO + cow over landscape), company, products, why bitsbeam
├── about.html            # about bitsbeam
└── assets/
    ├── application.css   # shared with cosmonats.bitsbeam.com — keep identical
    ├── application.js    # shared with cosmonats.bitsbeam.com — keep identical
    └── img/
        ├── logo.svg      # bitsbeam UFO mark
        ├── landscape.svg # hero band: city skyline + grass field
        └── *.svg         # product emblems: cosmonats, ferrum, cuprite, vessel
```

## Differences from cosmonats.bitsbeam.com

- `<body data-theme="bitsbeam">` swaps the accent to alien green (see section 5 of application.css).
- The tractor-beam gradient in the hero SVG is green to match.
- `.bb-*` classes (section 5 of application.css) give the company layout; `data-abduct` on the hero scene
  enables the occasional cow abduction (section 6 of application.js).

## Run locally

Open `index.html` in a browser, or serve the folder:

```sh
bundle install
bundle exec rake        # http://localhost:8000, override with PORT=3000
```

## Add a product

Duplicate a `.bb-product` in the matching `.bb-group` of `#products`, set its `--craft` accent, bump the
"N crafts in orbit" heading and add it to the footer's Products column.

## Deploy

GitHub Pages serves the folder as-is (`CNAME` → bitsbeam.com). Cosmonats links point to https://cosmonats.bitsbeam.com.

## License

MIT © bitsbeam
