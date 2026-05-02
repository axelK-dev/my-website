# FictionTown Book Club Website

> A calm, readable, and structured web experience designed for a fictional community book club.

---

## Overview

This project is a multi-page website created for the fictional *FictionTown Book Club*. The goal of this assignment is to demonstrate how HTML structure and CSS styling work together to create a clean, readable, and user-friendly website.

This project emphasizes clarity, accessibility, and consistency rather than overly complex design.

---

## Project Structure

```
my-website/
│
├── index.html
├── events.html
├── locations.html
├── about.html
│
├── styles/
│   └── styles.css
│
└── images/
    └── bookclub-placeholder.jpg
```

---

## Live Website vs Repository

This project exists in two important locations:

### GitHub Repository (Code Storage)

This is where all files are stored and version-controlled.

Example:
```
https://github.com/axelK-dev/my-website
```

---

### Live Website (GitHub Pages)

GitHub Pages allows the project to be hosted as a real website on the internet.

The live site follows this format:
```
https://axelK-dev.github.io/my-website/
```

- This version is viewable in a browser
- It reflects the HTML and CSS files in the repository
- Changes pushed to GitHub update the live site automatically

---

## Deployment Process

To publish the site using GitHub Pages:

1. Open the repository on GitHub
2. Go to **Settings**
3. Select **Pages**
4. Under **Source**, choose:
   - Branch: `main`
   - Folder: `/ (root)`
5. Save settings

GitHub then generates a public URL for the live site.

---

## CSS Implementation

The site uses an **external stylesheet** located at:

```
styles/styles.css
```

This separates content (HTML) from presentation (CSS), improving organization and maintainability.

---

## Selector Usage (Assignment Requirements)

### Type Selector
```css
body {
```
- Sets global font, spacing, and background

---

### Class Selector
```css
.highlight-section {
```
- Highlights important content visually
- Used for emphasis in key sections

---

### Relational Selector (Descendant)
```css
nav ul li {
```
- Targets list items inside navigation


---

### Combination Selector
```css
header h1 {
```
- Styles a specific element *within* another element

Additional example:
```css
.highlight-section h2 {
```

---

### Pseudo-Class Selector
```css
nav a:hover {
```
- Adds interaction when users hover over links

---

### Attribute Selector
```css
img[alt] {
```
- Targets images with alt text
- Reinforces accessibility practices

---

## Typography Choices

The following font properties are used:

- `font-family`: Arial, sans-serif
- `font-size`: uses `rem` for scalability
- `line-height`: improves readability

---

## Measurement Units

Only **relative units** are used:

- `rem` → spacing and font sizing
- `ch` → readable line lengths
- `%` → responsive images

---

## Color Usage

All colors are defined using hex values:

- `#faf9f7` → background
- `#3b5a40` → headings
- `#3b7d4c` → hover effects
- `#222222` → text

The palette supports a calm and readable design.

---

## Layout Decisions

- Content is centered using `max-width: 70ch`
- Sections are spaced evenly for readability
- Navigation is simple and vertical
- Padding creates balance and breathing room

---

## Accessibility Considerations

- Images include descriptive `alt` attributes
- Hover states improve navigation clarity
- Text contrast supports readability
- Semantic HTML improves structure

---

## Reflection

This project demonstrates how CSS helps:

- Build visual hierarchy
- Improve readability
- Add user interaction
- Maintain consistency across pages

The focus was on creating a stable, thoughtful user experience rather than adding unnecessary complexity.

---


- **GitHub Repository URL:**  
  https://github.com/axelK-dev/my-website

- **Live GitHub Pages URL:**  
  https://axelK-dev.github.io/my-website/

---
________________________________________
