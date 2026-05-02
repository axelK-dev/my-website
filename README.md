# FictionTown Book Club Website

> A calm, readable, and structured web experience designed for a fictional community book club.

---

## Overview

This project is a multi-page website created for the fictional *FictionTown Book Club*. The goal of this assignment is to demonstrate how HTML structure and CSS styling work together to create a clean, readable, and user-friendly website.

Across multiple modules, this project was expanded to include:

- CSS styling and selector usage
- Layout and spacing control
- Flexbox-based organization
- Section-specific styling using nested selectors

The design emphasizes clarity, readability, and intentional structure.

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

### GitHub Repository

https://github.com/axelK-dev/my-website/

---

### Live Website (GitHub Pages)

https://axelK-dev.github.io/my-website/

- This is the deployed version of the site
- Reflects the current HTML and CSS in the repository
- Updates automatically when changes are pushed

---

## Deployment Process

1. Push changes using:
   ```bash
   git add .
   git commit -m "update"
   git push
   ```
2. GitHub Pages builds and publishes the site
3. View the live site in a browser

---

## CSS Implementation (Module 4 Requirements)

The site uses an external stylesheet:

```
styles/styles.css
```

### Selector Usage

Type selector: line 5 (body)  
Class selector: line 86 (.highlight-section)  
Relational selector: line 48 (nav ul li)  
Combination selector: line 25 (header h1)  
Pseudo-class: line 58 (nav a:hover)  
Attribute selector: line 102 (img[alt])  

---

## CSS Design Choices

### Typography
- font-family
- font-size
- line-height

These improve readability and create a consistent text experience.

---

### Color System
- #faf9f7 (background)
- #3b5a40 (headings)
- #3b7d4c (interaction)
- #222222 (text)

---

### Layout
- Centered content using max-width
- Consistent spacing with margin and padding
- Section separation for readability

---

## Module 5: Layout and Flexbox Expansion

### Section Focus

The section styled most intentionally was the highlighted content section.

This section was chosen because it represents grouped information that benefits from visual separation and emphasis.

---

### Styled Section Container

The selected section includes:

- Background color distinct from page
- Padding for internal spacing
- Margin for separation
- Border accent for visual identity

This creates a clear content block that improves readability and structure.

---

### Flexbox Usage

Flexbox was applied to organize grouped content.

Key properties used:

- display: flex
- justify-content
- align-items
- gap

Flexbox changed the layout from a vertical stack to a more structured and responsive arrangement, improving alignment and spacing.

---

### Image Styling

One image was styled with:

- max-width for responsiveness
- border-radius for softness
- centered layout

This improves visual consistency and presentation.

---

## Advanced CSS Selectors Challenge

### Section Focus

The highlight-section was used to explore advanced selector behavior.

---

### Task 1: Section-Specific Styling

Selectors such as:

```css
.highlight-section h2
.highlight-section p
```

allow styling only inside that section without affecting global elements.

---

### Task 2: Nested Lists and Links

Inside the section:

```css
.highlight-section ul li
.highlight-section a:hover
```

These override global styles only within the section.

---

### Task 3: Descendants vs Direct Children

```css
.highlight-section p
.highlight-section > p
```

- descendant affects all nested elements
- direct child affects only immediate children

---

### Task 4: Combining Classes and Elements

```css
.highlight-section img
```

Images inside the section are styled differently than global images.

---

### Task 5: Pseudo-Class Precision

```css
.highlight-section a:hover
```

Applies hover effects specifically inside the section rather than globally.

---

### Task 6: Reducing Redundancy

Repeated styles were consolidated using more specific selectors, reducing duplication and improving maintainability.

---

## Reflection

### What section did you focus on styling and why?

The highlight section was the focus because it represents grouped content that benefits from visual separation and structure.

---

### How did Flexbox change the layout?

Flexbox improved alignment and spacing between elements, making the layout more controlled and visually balanced compared to a simple vertical flow.

---

### One CSS rule I feel confident about

```css
nav ul li
```

This relational selector clearly demonstrates how structure influences styling.

---

### One CSS rule that was confusing at first

```css
.highlight-section > p
```

Understanding the difference between descendant and direct child selectors required careful observation of how nesting affects styling.

---

### Why are nested selectors more useful than global styling?

Nested selectors allow precise control, preventing unwanted styling across the entire page and enabling section-specific design.

---

### One selector that felt especially powerful

```css
.highlight-section a:hover
```

It demonstrates how styling can be both contextual and interactive.

---

### One selector that took time to understand

The difference between:

```css
section p
section > p
```

Understanding this clarified how CSS reads hierarchy.



