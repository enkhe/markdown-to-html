# Markdown → HTML Live Editor

A single-file, zero-install live editor that renders Markdown to HTML with full syntax highlighting.  
Open `md-to-html.html` in any modern browser — no server, no build step, no dependencies to install.

**Author:** [Enkhe](https://github.com/enkhe)  
**License:** MIT  
**© 2026**

\---

## Features

### Editor

* Live split-pane layout — editor left, rendered HTML right
* Resizable divider with split position saved across sessions
* Debounced auto-render (80 ms) or manual render (`Ctrl+Enter`)
* Synchronized scroll — editor and preview track each other
* Tab key inserts 4 spaces
* Drag \& drop `.md` / `.txt` files directly onto the editor

### Format Bar

One-click Markdown formatting buttons above the editor. Each button is toggle-aware: pressing it again removes the prefix/wrapper.

|Button|Markdown|Shortcut|
|-|-|-|
|**B**|`\*\*bold\*\*`|`Ctrl+B`|
|*I*|`\*italic\*`|`Ctrl+I`|
|~~S~~|`\~\~strikethrough\~\~`|—|
|``c``|``inline code``|—|
|`</>`|````code block````|—|
|H1 / H2 / H3|`# ` / `## ` / `### `|—|
|🔗|`\[text](url)`|`Ctrl+K`|
|🖼|`!\[alt](url)`|—|
|`"`|`> blockquote`|—|
|`•`|`- bullet`|—|
|`1.`|`1. numbered`|—|
|☑|`- \[ ] task`|—|
|`—`|`---` horizontal rule|—|
|⬛|Inserts a 3-column table template|—|

### Syntax Highlighting

Fenced code blocks are highlighted via [highlight.js](https://highlightjs.org/) with a VS Code–inspired token palette (separate light and dark themes).

Supported languages include: JavaScript, TypeScript, Python, Java, C#, Kotlin, Swift, Rust, Go, Scala, Dart, Bash, SQL, HTML, CSS, JSON, YAML, Dockerfile, PowerShell, and all auto-detected languages.

Every code block renders with a **language label** and a **Copy** button.

### Export \& Share

|Action|Details|
|-|-|
|Export HTML|Self-contained `.html` file with inline CSS, themed (dark or light)|
|Print preview|Opens rendered HTML in a new tab and triggers `window.print()`|
|Copy HTML source|Full standalone HTML copied to clipboard|
|Copy rendered text|Plain text (no markup) copied to clipboard|
|Share URL|Document encoded with LZString into the URL hash — paste and share, no server needed|

### UX

* Dark / light theme toggle with `localStorage` persistence
* Auto/Manual render mode badge (`Ctrl+M`)
* New button with "Discard?" confirmation
* Pinned CDN versions (marked `18.0.3`, highlight.js `11.11.1`, LZString `1.5.0`)
* Touch-friendly divider for tablets
* `@media (prefers-reduced-motion)` support

\---

## Keyboard Shortcuts

|Shortcut|Action|
|-|-|
|`Ctrl+O`|Open `.md` file|
|`Ctrl+S`|Save Markdown source|
|`Ctrl+E`|Export as HTML|
|`Ctrl+Enter`|Force render now|
|`Ctrl+M`|Toggle auto / manual render|
|`Ctrl+B`|Bold|
|`Ctrl+I`|Italic|
|`Ctrl+K`|Insert link|
|`Tab`|Insert 4 spaces|
|`?` / `F1`|Keyboard shortcut help|
|`Escape`|Close modal / dropdown|
|Drag file onto editor|Open `.md` file|

\---

## Getting Started

1. Download or clone this repo.
2. Open `md-to-html.html` in Chrome, Edge, Firefox, or Safari.
3. Type or paste Markdown in the left pane — the rendered HTML appears live on the right.

No npm, no bundler, no internet connection required after the CDN assets are cached.

\---

## Exported HTML

The HTML export is a fully self-contained document with:

* Inline CSS matching the current dark/light theme
* All heading, table, blockquote, code block, and list styles embedded
* A footer noting the source file name and export timestamp
* No external dependencies (works fully offline)

\---

## File Format

The editor opens and saves `.md` files (plain text, GitHub-Flavored Markdown).  
It also accepts `.markdown` and `.txt` extensions.

\---

## License

MIT © 2026 [Enkhe](https://github.com/enkhe)

