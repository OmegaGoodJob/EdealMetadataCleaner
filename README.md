# Edeal Metadata Cleaner

Edeal Metadata Cleaner is a small desktop application built with [Electron](https://electronjs.org/) that removes unwanted pieces from E‑Deal metadata XML files. It reads the file line by line and deletes each `<reference>` block whose `radical` attribute matches a user defined list.

## Features

* Simple graphical interface.
* Drag & drop or file selector to choose the metadata file.
* Progress bar with the option to stop cleaning at any time.
* Configurable list of radicals stored in a local settings file.
* The cleaned file is written next to the original with the `.new` extension.

## Installation

1. Install [Node.js](https://nodejs.org/) (tested with Node v7).
2. Install the dependencies:
   ```bash
   npm install
   ```

## Usage

Run the application with Electron:

```bash
npx electron .
```

When the window appears:

1. Select or drag your metadata XML file.
2. Click **Nettoyer** to start cleaning. The progress bar indicates the current percentage.
3. Use **Options > Paramètres** to edit the radicals list. Each radical corresponds to the first three characters of a `<reference>` tag.
4. Once finished, the cleaned file is created beside the original with the `.new` suffix.

## Project structure

* `app.js` – Electron entry point.
* `api/metadatacleaner/mcengine.js` – Main cleaning engine.
* `routes/` – Menu configuration.
* `views/` – HTML interfaces.
* `public/` – Static assets (JS, CSS, fonts).

## Development

Feel free to modify the views or the cleaning logic. Pull requests and issues are welcome.

## License

MIT
