# Markdown Tabs Viewer

This is a simple and professional web app that allows users to view Markdown content in two synchronized tabs: the rendered HTML view and the original Markdown source. It supports loading Markdown content from a URL specified in the `?url=` query parameter and displays the active source URL or default label accordingly.

Additionally, it features a live-updating word count badge, formatted using `Intl.NumberFormat` for locale-sensitive number formatting.

## Features

- Two tabs: **Rendered** (HTML) and **Source** (original Markdown) with synchronized content
- Load Markdown content from external URLs via the `?url=` query parameter
- Display the current source URL or a default label
- Live word count badge updated on every render
- Responsive and accessible UI

## How to Use / Run

1. Clone or download all the project files.
2. Open `index.html` in any modern web browser (no server needed for local Markdown input).
3. To load Markdown from an external URL, append `?url=ENCODED_URL` to the address bar, e.g.:  
   `file:///path/to/index.html?url=https%3A%2F%2Fraw.githubusercontent.com%2Fuser%2Frepo%2Fbranch%2FREADME.md`
4. Use the **Rendered** and **Source** tabs to toggle views. Changes in the Markdown source tab immediately update the rendered preview.

## Technical Details

- Plain JavaScript (ES6+) without dependencies
- Uses the modern `fetch` API to load external Markdown content
- Tabs implemented with buttons inside a container
- Markdown is rendered using a lightweight embedded `marked` parser (included as a small JS snippet in the script) for simplicity and performance
- Word count is updated live on source changes
- Number formatting via `Intl.NumberFormat` for locale-aware comma separators
- Basic CSS included for professional styling and clear UX

## Dependencies

None external. All code and markdown rendering logic is embedded within the project files.

## License

MIT License