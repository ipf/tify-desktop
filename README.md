# TIFY Desktop

## About

This is a desktop application for the TIFY IIIF-Viewer.

## Live Development

Requirements for building the Application:
* go-version: ^1.18
* node-version: ^16
* Wails: `go install github.com/wailsapp/wails/v2/cmd/wails@latest`

To run in live development mode, run `wails dev` in the project directory. In another terminal, go into the `frontend`
directory and run `npm run dev`. The frontend dev server will run on http://localhost:34115. Connect to this in your
browser and connect to your application.

## Building

To build a redistributable, production mode package, use `wails build`.
