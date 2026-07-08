# Character Counter

A clean, dark-themed live character counter built with vanilla HTML, CSS, and JavaScript. Type into the text area and watch the count, progress bar, and color states update in real time — just like the composer on Twitter/X.

## Features

- **Live character count** — updates instantly as you type (`input` event, no extra libraries)
- **Progress bar** — visually fills up as you approach the character limit
- **Color-coded states**
  - Blue — normal typing
  - Amber (`warning`) — 80% to 99% of the limit
  - Red (`danger`) — at the limit (100%)
- **280-character limit** by default, enforced natively via the `maxlength` attribute
- **Responsive, dark UI** with smooth transitions and no external dependencies

## Demo

Open `index.html` in any browser — no build step or server required.

## File Structure

```
CHARACTER-COUNTER/
├── index.html   # Markup: textarea, counter display, progress bar
├── style.css    # Dark theme styling, color states, transitions
├── script.js    # Character counting logic and state updates
└── README.md
```

## How It Works

1. `script.js` reads the `maxlength` attribute off the textarea to determine the limit.
2. On every keystroke (`input` event), it calculates `currentLength / maxLength * 100`.
3. The counter text and progress bar width are updated to match.
4. A `warning` class is applied between 80–99% of the limit, and a `danger` class at 100%, changing the color of both the counter text and progress bar.

## Getting Started

Clone the repo and open the HTML file directly:

```bash
git clone https://github.com/gaurav10prince-cell/CHARACTER-COUNTER.git
cd CHARACTER-COUNTER
open index.html   # or just double-click it
```

## Customization

- **Change the limit**: update `maxlength="280"` on the `<textarea>` in `index.html`.
- **Change thresholds**: edit the `percentage >= 80` and `percentage >= 100` checks in `script.js`.
- **Change colors**: update the CSS variables/values in `style.css` (`.warning`, `.danger`, and `.progress-fill`).

## Tech Stack

- HTML5
- CSS3 (Flexbox, transitions)
- Vanilla JavaScript (no frameworks or dependencies)

## License

This project is licensed under the [MIT License](LICENSE).
