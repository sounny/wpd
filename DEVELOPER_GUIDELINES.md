# WebPlotDigitizer Developer Guidelines

Please note the following before you begin:
- By contributing to WebPlotDigitizer, you are automatically agreeing to the [Contributor License Agreement](CONTRIBUTING.md).
- Open source doesn't automatically imply that this project is open for all kinds of contributions. Please consult with Ankit Rohatgi before considering to make any large contributions.

## Where to start?

Areas to contribute:
- Documentation and tutorial videos
- Language translations
- Unit tests or other tests
- Code cleanup
- Tooling for building, formatting etc.
- Bug fixes and pruning GitHub issues list
- New features

## Development Setup

It should be easy to setup any Linux distribution for development purposes, but Ubuntu is preferred. MacOS has a few different setup steps and is currently experimental. Windows is unsupported for development.

To install Ubuntu packages and download other dependencies, you can try the script [setupUbuntuDev.sh](setupUbuntuDev.sh).
To install MacOS packages and download other dependencies, you can try the script [setupMacOSDev.sh](setupMacOSDev.sh).

For other operating systems, please install the following dependencies manually:

UI (this fork):
- No build step required. Static HTML/CSS/JS served from the repository root.
- Third-party: PDF.js is loaded from a CDN in `index.html`.

Web Server:
- A recent Go compiler

Electron App:
- `electron-packager` npm package to create packages for distributions
- `wine` on Linux systems to create Windows distributions
- Run `npm install` in the electron folder to fetch any other dependencies

## Building Source

**Building HTML5 Source**

This fork does not require a build step. Open `index.html` directly or serve the folder via a static HTTP server.

**Web Server**

PHP backend has now been replaced with a simple Go server. To start the server do the following:

    cd webserver
    cp settings.json.example settings.json
    # edit settings.json as needed
    go build
    ./webserver

You can now open WebPlotDigitizer in your web browser.

The Go based server will be extended to include typical server side features like server-side data storage, remote APIs etc.

**Electron App**

To run the electron app, follow these steps:

    cd electron
    npm install
    npm start

    At the moment, this is only a basic implementation. If you are familiar with electron app development, feel free to contribute here.

On a Linux development machine, you will also need `wine` to build the Windows app. To build the apps, run:

    cd electron
    npm install
    npm run build # Windows, Mac and Linux
    ./build-mac.sh # MacOS only (may require global install of `electron-packager` from `npm`)

This will create apps for Mac, Windows and Linux.

## Unit Tests

This fork currently does not include the legacy QUnit/Karma test runner. If you add tests, prefer lightweight browser-based test harnesses or simple integration checks.

## Coding Style

- **Javascript**: ES6 with [AirBnB's style guide](https://github.com/airbnb/javascript) is recommended. A lot of older code does not follow this style and should be updated eventually.

To run automatic formatting on the Javascript and C++ code, use this command:

    cd app
    npm run format

Or, alternatively, run the [format.sh](app/format.sh) script in the `app` folder.

## Scripts

Custom JS scripts can be loaded into WebPlotDigitizer and executed. See [script_examples](script_examples/README.md) for more details.

## Docker

Legacy Docker and research artifacts have been pruned in this fork.

## Internationalization (Language Translations)

Translations in this fork are provided inline (minimal i18n strings) in `index.html`.

## Documentation, Tutorial Videos

Good documentation and tutorials are severely lacking and any help would be highly appreciated. The LaTeX source for the current user manual is in the `docs/latex` folder.
