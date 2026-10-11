# bitsbeam.com

Company site for bitsbeam: UFO + cow hero, "why bitsbeam", the fleet (products) and an about page.
Plain static HTML / CSS / JS — no build step, no dependencies.
The Cosmonats site lives next door in `../cosmonats.bitsbeam.com/` and shares `assets/application.css` +
`application.js` — keep both copies identical.

## Structure

```
/
├── index.html            # hero (UFO beaming the cow), why bitsbeam, fleet
├── about.html            # about bitsbeam
└── assets/
    ├── application.css   # shared with cosmonats.bitsbeam.com — keep identical
    ├── application.js    # shared with cosmonats.bitsbeam.com — keep identical
    └── img/
        ├── logo.svg      # bitsbeam UFO mark
        └── *.svg         # fleet emblems: cosmonats, ferrum, cuprite, vessel
```

## Differences from cosmonats.bitsbeam.com

- `<body data-theme="bitsbeam">` swaps the accent to alien green (see section 5 of application.css).
- The tractor-beam gradient in the hero SVG is green to match.

## Run locally

Open `index.html` in a browser, or serve the folder:

```sh
bundle install
bundle exec rake        # http://localhost:8000, override with PORT=3000
```

## Add a craft to the fleet

Duplicate a `.craft-card` in `#fleet`, set its `--craft` accent, bump "Craft #00N" and the "N crafts in orbit" counter.

## Deploy

GitHub Pages serves the folder as-is (`CNAME` → bitsbeam.com). Cosmonats links point to https://cosmonats.bitsbeam.com.

## License

MIT © bitsbeam
