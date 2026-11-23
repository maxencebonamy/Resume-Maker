# CV-Maker

A one-page CV written in HTML and CSS, laid out for A4.

The page is a static document: edit `index.html`, open it in a browser, and print or export it to PDF. It is meant for people who want to control the layout of their CV directly in code.

## Table of contents

- [CV-Maker](#cv-maker)
	- [Table of contents](#table-of-contents)
	- [How it works](#how-it-works)
	- [Tech stack](#tech-stack)
	- [Repository structure](#repository-structure)
	- [Prerequisites](#prerequisites)
	- [Installation](#installation)
	- [Running locally](#running-locally)
	- [Example](#example)
	- [License](#license)

## How it works

1. **Content**: all text lives in `index.html`: contact block, presentation, personal info, languages, skills, training and experience, hobbies.
2. **Layout**: the `body` is sized to 21 cm by 29.7 cm (A4) with 50 px of padding. Blocks are arranged with flexbox through the `row` and `column` classes.
3. **Skill levels**: each skill shows five dots. A dot with the `transparent` class counts as empty.
4. **Icons**: icons come from Font Awesome, loaded from its kit script in the page head.
5. **Theme**: colors and the font are declared once in `css/utils.css` (`--background`, `--light`, `--secondary`, `--primary`, and the `Klik-Light` font).

## Tech stack

| Layer | Technologies |
| --- | --- |
| Markup | HTML5 |
| Styling | CSS3 (flexbox, custom properties) |
| Icons | Font Awesome (kit script) |
| Font | Klik Light (`assets/font/Klik-Light.otf`) |

## Repository structure

```
.
├── assets/
│   ├── font/        Klik-Light.otf
│   └── img/         profile.png
├── css/
│   ├── div.css      Styles of the layout blocks
│   ├── style.css    Entry stylesheet: body, dividers, imports
│   └── utils.css    Font and color variables
├── output/          Rendered example of the CV
├── index.html       CV content
```

`css/style.css` imports `css/utils.css` and `css/div.css`; `index.html` only links `css/style.css`.

## Prerequisites

- A web browser
- Internet access, so the Font Awesome kit script can load the icons

## Installation

```bash
git clone git@github.com:maxencebonamy/CV-Maker.git
cd CV-Maker
```

To use your own photo, replace `assets/img/profile.png`.

## Running locally

Open `index.html` in a browser.

```bash
open index.html
```

To produce a PDF, use the browser print dialog with the A4 paper size and background graphics enabled.

## Example

![Rendered CV](output/image.png)

## License

This project is licensed under the [MIT License](LICENSE).
