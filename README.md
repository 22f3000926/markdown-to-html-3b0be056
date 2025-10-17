# Markdown to HTML Static Page Renderer

This project provides a static web page that converts a markdown file (`input.md`) to HTML using the `marked` library, then renders the resulting HTML into a page element with the ID `#markdown-output`. Additionally, it integrates `highlight.js` to apply syntax highlighting to any code blocks in the rendered markdown.

## Features
- Parses `input.md` on page load to HTML.
- Renders parsed HTML inside the `#markdown-output` container.
- Automatically highlights code blocks leveraging `highlight.js`.
- Uses CDN links for `marked` and `highlight.js` for simplicity and performance.

## How to Use / View
1. Place your markdown content into the `input.md` file.
2. Open `index.html` in any modern web browser.
3. The page will render the markdown content as HTML with syntax-highlighted code blocks.

## Technical Details / Dependencies
- Uses [marked](https://github.com/markedjs/marked) (v4.x) for markdown parsing.
- Uses [highlight.js](https://highlightjs.org/) (latest) for code syntax highlighting.
- The markdown content is fetched at runtime via `fetch`.

## Notes
- The solution fetches `input.md` using Fetch API, so accessing the page locally may require a web server due to CORS restrictions in some browsers.
  - Recommended running:
    - Using Python 3+: `python -m http.server`
    - Or any static server of your choice.
- Highlight.js automatically detects the language of code blocks; you can customize it with supported languages if desired.

## License

MIT License