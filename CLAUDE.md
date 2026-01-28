# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Data dashboard example project using Express.js backend with static HTML/CSS dashboards. All charting is done with custom CSS (no chart libraries).

## Commands

```bash
npm i              # Install dependencies
node server.js     # Start dev server on http://localhost:3000
```

## Architecture

**Backend:** Express.js server (`server.js`) serving static files from `docs/`

**Frontend:** Pure HTML5/CSS3 dashboards with:
- Custom CSS-based bar charts (div elements with gradients, no Chart.js)
- Responsive CSS Grid layouts with mobile breakpoints
- Card-based UI with status badges

**Dashboard Structure:**
- `docs/index.html` - Navigation hub
- `docs/1/index.html` - Real estate dashboard (山田不動産)
- `docs/2/index.html` - Used car sales dashboard (中古自動車)
- `docs/3/index.html` - Home electronics retail dashboard (家電販売)
- `docs/4/`, `docs/5/`, `docs/6/` - Empty placeholders

## Key Patterns

**Accessibility:** Dashboards use ARIA labels with data context, semantic HTML, proper heading hierarchy, and aria-hidden for decorative elements.

**CSS Classes:** Status badges use domain-specific naming (e.g., `.for-sale`, `.in-negotiation`, `.sold` for real estate).

**Charts:** Bar charts are rendered using `<div>` elements with CSS `height` percentages and linear gradients - no JavaScript charting libraries.
