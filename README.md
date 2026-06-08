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

## Module 4: Layout and Flexbox Expansion

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
## CSS Animation: Ken Burns Effect (Advanced Styling)

### Overview

A subtle Ken Burns-style animation was implemented entirely using CSS to enhance visual engagement across the site without relying on JavaScript.

The effect introduces gentle motion through controlled zoom and panning, creating a calm and cinematic presentation for images.

---

### Implementation Approach

The animation is applied using a reusable image class:

```css
.ken-burns-pic {
  width: 100%;
  height: 100%;
  object-fit: cover;
  object-position: center;
  animation: kenburns 12s ease-in-out infinite;
}
```

---

### Keyframe Animation

The effect is achieved using CSS `@keyframes`:

```css
@keyframes kenburns {
  0% {
    transform: scale(1.02);
  }

  100% {
    transform: scale(1.08);
  }
}
```

---

### Container Structure

Images are placed inside a controlled frame:

```css
.image-frame {
  overflow: hidden;
  height: 300px;
}
```

This ensures that:

- The image fills the container
- Overflow is clipped cleanly
- The animation appears as a controlled camera movement

---

### Design Considerations

Several design decisions were made to maintain visual clarity:

- Minimal zoom range (1.02–1.08) to reduce aggressive cropping
- Slow animation timing for a calm user experience
- Consistent default focus using `object-position: center`

---

### Image-Specific Adjustments

Some images required custom tuning due to composition differences:

```css
.library-kenburns {
  object-position: 50% 30%;
  animation: libraryBurns 15s ease-in-out infinite;
}
```

This allows more of the image to remain visible and preserves important visual areas.

---

### Challenges and Solutions

**Inconsistent Cropping**  
Images with different aspect ratios behaved unpredictably when scaled.

- Reduced zoom intensity
- Adjusted focal points using `object-position`
- Selected images with better composition

**Too Many Variables**  
Balancing layout, motion, and cropping made troubleshooting difficult.

- Isolated test sections were created
- One image was tuned at a time
- Dedicated classes were used for special cases

---

##### Key Learning Outcome: This feature demonstrated that CSS alone can create dynamic visual effects, but effective results depend on balancing animation, layout constraints, and image composition.
---
### Module 5 — Page Layout + Box Model / Padding Lessons

**Design goal:** keep text readable inside consistent “cards” while using the About page to demonstrate a **2‑column layout**. 

---

#### Requirements → Where my code shows them

###  Padding and/or margins on 3+ elements (aesthetic spacing)
- **Header padding** creates breathing room: `header { padding: 2rem 1.5rem; }`   
- **Main padding** creates gutters: `main { padding: 2rem 1.5rem; }`   
- **Card padding + spacing**: `.content-box { padding: 1.5rem; margin-bottom: 2rem; }`   
- **Row spacing**: `.about-layout { margin-bottom: 2rem; }`   

###  Borders on at least one element
- Borders applied to every card for clear separation:
  - `.content-box { border: 0.1rem solid #e3e1db; }`   

###  Background gradient (doesn’t harm readability)
- Background gradient is applied to the whole page:
  - `body { background: linear-gradient(...); }`   
- Readability stays high because text sits on white `.content-box` cards:
  - `.content-box { background-color: #ffffff; }`   

###  2nd page uses a 2‑column layout
- About page uses **two separate float-based 2‑column rows**:
  - Row 1: `.about-image` + `.about-mission`
  - Row 2: `.about-history` + `.about-values`   

---

## Exact code patterns I kept (the techniques that matter)

### 1) About page layout scaffold (HTML: wrapper rows + column boxes)
I grouped each pair of columns into a wrapper row (`.about-layout`). 

```html
<!-- INTRO (full-width card) -->
<section class="content-box">
  ...
</section>

<!-- ROW 1 (two columns) -->
<section class="about-layout">
  <div class="about-image content-box">
    ...
  </div>

  <div class="about-mission content-box">
    ...
  </div>
</section>

<!-- ROW 2 (two columns) -->
<section class="about-layout">
  <div class="about-history content-box">
    ...
  </div>

  <div class="about-values content-box">
    ...
  </div>
</section>
```

**Why this is a best practices habit:** wrapping columns into explicit “rows” makes layout predictable and prevents random stacking. 

---

### 2) Float-based columns (CSS: float + width + gap)
I used floats and widths to make the boxes sit side-by-side. 

```css
/* Row wrapper */
.about-layout {
  overflow: hidden;
  margin-bottom: 2rem;
}

/* FIRST ROW */
.about-image {
  float: left;
  width: 40%;
  margin-right: 2%;
}

.about-mission {
  float: left;
  width: 58%;
}

/* SECOND ROW */
.about-history {
  float: left;
  width: 48%;
  margin-right: 2%;
}

.about-values {
  float: left;
  width: 48%;
}
```

**Three “basic” float rules to remember:**
1. `float: left` turns boxes into columns.   
2. `% width` decides how much space each column takes.   
3. `margin-right` creates the gap between columns.   

---

### 3) Float clearing (CSS: the wrapper must not collapse)
I used the wrapper clear technique:

```css
.about-layout { overflow: hidden; }
```

This keeps each row wrapper “containing” its floated children. 

---

### 4) Mobile readability fallback (CSS: stack on small screens)
```css
@media (max-width: 768px) {
  .about-image,
  .about-mission,
  .about-history,
  .about-values {
    float: none;
    width: 100%;
    margin-right: 0;
  }
}
```
This preserves readability by reverting to one column on small screens. 

---

### 5) Container width (CSS: columns need room to exist)
```css
main {
  max-width: 900px;
  margin: 0 auto;
  padding: 2rem 1.5rem;
}
```
If `main` is too narrow, even correct float code will stack. 

---

## The padding lesson (the real concept)
My cards add padding and borders: 

```css
.content-box {
  padding: 1.5rem;
  border: 0.1rem solid #e3e1db;
}
```

**Key lesson:** padding/borders affect how much space a column *effectively* consumes in a row.  
So even if widths look fine, layout can stack when:
- the container is narrow, OR
- the total “effective width” (content + padding + border + margins/gaps) exceeds the row. 

---

## DevTools / Inspector: the debugging move to use every time
If columns stack unexpectedly, the fastest checks are:

1. Inspect `.about-image` (or `.about-history`) → confirm `float: left` is applied.   
2. Look at the **box model** panel → see content size vs padding vs border (why it doesn’t fit).   
3. Inspect `main` → confirm it has `max-width: 900px` and padding (container constraints).   
4. Inspect `.about-layout` → confirm `overflow: hidden` (row clearing).   

---

## Future checklist (what I should remember)
-  Always group columns into row wrappers (`.about-layout`).   
-  Floats need: `float + width + gap`, plus a clear (`overflow: hidden`).   
-  Container width matters (`main max-width`).   
-  Padding/border are part of layout reality (they can cause stacking).   
-  Always include a mobile stack fallback.   

---
## 3D Carousel (CSS-Only) — Featured Reads

## Overview

This feature implements a **3D rotating carousel** that displays five fictional book titles using **pure HTML and CSS (no JavaScript)**.

The carousel appears on the **Home page** under *Featured Reads*, providing a visual introduction to the types of books explored by the FictionTown Book Club.

---

## Design Intent

The carousel is intentionally placed within the page flow:

Welcome → Featured Reads (visual) → Upcoming Highlights → Community

- **Welcome** introduces the club  
- **Carousel** shows what the club reads  
- **Highlights** provide structured information  
- **Community section** adds emotional context  

This approach balances visual interest with readability.

---

## How It Works

### 1. Establishing a 3D Viewing Context

The `.scene` container uses `perspective`:

    .scene {
      perspective: 1000px;
    }

- This creates depth
- Elements farther away appear smaller

---

### 2. Creating a 3D Space

The carousel preserves depth:

    .carousel {
      transform-style: preserve-3d;
    }

- Without this, everything would appear flat

---

### 3. Positioning Cards in a Circle

Each card is rotated and pushed outward:

    .card:nth-child(1){ transform: rotateY(0deg) translateZ(300px); }
    .card:nth-child(2){ transform: rotateY(72deg) translateZ(300px); }
    .card:nth-child(3){ transform: rotateY(144deg) translateZ(300px); }
    .card:nth-child(4){ transform: rotateY(216deg) translateZ(300px); }
    .card:nth-child(5){ transform: rotateY(288deg) translateZ(300px); }

Key concept:

360° ÷ 5 cards = 72° spacing

- `rotateY()` places the card around the circle  
- `translateZ()` pushes it outward  

This creates a circular 3D arrangement.

---

### 4. Rotating the Carousel

The carousel rotates using animation:

    @keyframes spin {
      from { transform: translateZ(-300px) rotateY(0deg); }
      to   { transform: translateZ(-300px) rotateY(360deg); }
    }

    .carousel {
      animation: spin 20s linear infinite;
    }

- The entire structure rotates as one unit  
- This creates a smooth orbiting effect  

---

## Accessibility Consideration

Motion can be reduced for users who prefer it:

    @media (prefers-reduced-motion: reduce) {
      .carousel {
        animation: none;
      }
    }

- This improves accessibility and usability

---

## Visual Design Choices

- Soft background (`#faf8f4`) → calm reading aesthetic  
- Serif font (Georgia) → literary tone  
- Subtle shadows → gentle depth  

The goal was to keep the effect **clean and readable**, not distracting.

---

## Constraints & Decisions
  
- CSS-only animation used  
- Semantic HTML maintained  
---

## Key Takeaways

This feature demonstrates:

- CSS 3D transforms (`rotateY`, `translateZ`)
- Animation with `@keyframes`
- Depth using `perspective`
- Structured layout integration
- Accessibility awareness

---

#### Reflection

This component reinforces an important idea:

Structure enables creativity.

###### By organizing the page first, the carousel could be added as a purposeful visual element rather than a distraction.

---

#### Theme & Layout System

This project implements a multi-page theming system using **HTML, CSS, and JavaScript**, with a focus on stability and scalability.

---

#### Structure (HTML)

- Shared layout across all pages (`header`, `main`, `footer`)
- Page identity via body class:

```html
<body class="page-about">
```

### Theme System (CSS Variables)

Global styles are controlled with variables:
```

:root {
--bg: ...;
--text: ...;
--accent: ...;
}
[data-theme="dark"] {
--bg: #121212;
}
```
- One change updates the entire site  
- Enables light, dark, and neon themes  

---

### Theme Persistence (JavaScript)

User theme selection is saved and reused:


localStorage.setItem("theme", theme);

On page load:


const savedTheme = localStorage.getItem("theme");

- Theme carries across all pages  
- No re-selection required  

---

#### Page Variations

Each page can override specific variables:


body.page-about {
--accent: #845ec2;
}

**Result:**

Global theme + local variation  
→ consistent system with flexible identity  

---

#### Design Principles

- Layout and theme are separated  
- Components remain structurally stable  
- Themes affect *only* visual properties  

---

#### Goal

- One global theme system  
- Page-level customization  
- No duplication of styles  
- Easy to adjust without breaking layout  

---

#### Summary

- **HTML** → structure + page identity  
- **CSS** → layout + theme variables  
- **JavaScript** → interaction + persistence  
### Global Navigation + Theme System

#### Overview

A multi-page site with:
- Global navigation bar (same on every page)
- Theme switching (Light / Dark / Neon)
- Default theme: Light
- Theme persists across pages (session only)
- Hover-based dropdown menu

---

#### Navigation (Use on EVERY page)

```html
<nav>
  <ul class="navbar">
    <li><a href="index.html" class="active">Home</a></li>
    <li><a href="events.html">Events & Calendar</a></li>
    <li><a href="locations.html">Locations</a></li>
    <li><a href="about.html">About Us</a></li>

    <li class="dropdown">
      <span class="dropbtn">Themes</span>
      <ul class="dropdown-content">
        <li><button data-set-theme="light">Light</button></li>
        <li><button data-set-theme="dark">Dark</button></li>
        <li><button data-set-theme="neon">Neon</button></li>
      </ul>
    </li>
  </ul>
</nav>
```

---

#### CSS (Core Behavior)

```css
.navbar {
  display: flex;
  gap: 1rem;
  list-style: none;
  margin: 0;
  padding: 0;
}

.dropdown {
  position: relative;
}

.dropdown-content {
  display: none;
  position: absolute;
  list-style: none;
  background: white;
}

.dropdown:hover .dropdown-content {
  display: block;
}
```

---

#### JavaScript (Theme Handling)

```html
<script>
const theme = sessionStorage.getItem("theme");

if (theme) {
  document.documentElement.setAttribute("data-theme", theme);
}

document.querySelectorAll('[data-set-theme]').forEach(btn => {
  btn.addEventListener('click', () => {
    const t = btn.dataset.setTheme;
    document.documentElement.setAttribute("data-theme", t);
    sessionStorage.setItem("theme", t);
  });
});
</script>
```

---

### Rules

- Theme controls must use `<button>`
- Do not remove any theme options
- Nav + script must be identical on every page

---

### Behavior

```
Page load → Light (default)

User clicks theme →
  applies immediately
  saved for session

Navigate pages →
  same theme persists

Close browser →
  resets to Light
```

---

#### System Summary

- Consistent navigation structure
- Hover-driven dropdown interaction
- Explicit user-controlled themes
- Session-based persistence (no permanent override)
---
### Responsive Design Improvements (Media Queries)

To improve usability across different device sizes, two media queries were implemented:

#### Tablet Breakpoint
```css
@media (max-width: 768px)
```
and
#### Mobile Breakpoint
```
@media (max-width: 480px)
```
### Module 7 — Layout + Responsiveness Updates

#### Grid (Requirement)
Added grid layout for event cards:

```css
.events {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 2rem;
}
```

Responsive stack:

```css
@media (max-width: 768px) {
  .events {
    grid-template-columns: 1fr;
  }
}
```

---

#### Flexbox (Existing Structure)
Used for layout control:

```css
nav ul { display: flex; }
.about-layout { display: flex; }
```

---

#### Breakpoints (3+ Required)

```css
/* 900px → collapse 2-column layout */
@media (max-width: 900px) {
  .about-layout { flex-direction: column; }
}

/* 768px → stack grid */
@media (max-width: 768px) {
  .events { grid-template-columns: 1fr; }
}

/* 480px → mobile layout + nav fix */
@media (max-width: 480px) {
  nav ul { flex-direction: column; }
}
```

---

#### Mobile Dropdown Fix (Usability Issue)

Problem: absolutely positioned dropdown breaks in stacked nav

Fix:

```css
.dropdown-content {
  position: static;
  display: none;
  padding-left: 1rem;
}

.dropdown:hover .dropdown-content,
.dropdown:focus-within .dropdown-content {
  display: block;
}
```

---

#### Viewport Height (Requirement)

```css
main {
  min-height: 100vh;
}
```

Ensures all pages fill screen without adding extra content.

---

#### Key Fixes

- Converted dropdown from overlay → inline (mobile)
- Added grid without changing layout structure
- Introduced targeted breakpoints (900 / 768 / 480)
- Fixed CSS syntax issues (missing braces, invalid rules)
- Added purpose-based comments

---

#### Result

- Flex + Grid both implemented
- Layout stable across device sizes
- Navigation usable on mobile
- Pages meet viewport height requirement
- Design preserved (no structural rewrite)
### Final Layout Fixes

#### Grid Structure Fix

Initially, applying `display: grid` to `.events` caused the `<h2>` heading to be treated as a grid item, which broke layout alignment and constrained the event cards.

This was corrected by introducing a wrapper:

```html
<section class="events">
  <h2>Upcoming Events</h2>

  <div class="events-grid">
    <article class="event content-box">...</article>
    <article class="event content-box">...</article>
  </div>
</section>
```

And moving the grid styling to:

```css
.events-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 2rem;
}
```

This ensures only the event cards participate in the grid.

---

#### Card Consistency Fix

The second event initially lacked the card styling.

```html
<article class="event">
```

was corrected to:

```html
<article class="event content-box">
```

This applies consistent padding, borders, and shadows across both items.

---

#### Responsive Behavior

Media queries were used to stabilize layout behavior across screen sizes and ensure the design remained usable from desktop down to mobile widths. These adjustments helped prevent layout breakage and maintain consistent spacing and alignment.

---

#### Result

- Grid requirement satisfied without breaking layout
- Heading removed from grid flow
- Event cards align cleanly
- Images display at correct proportions across screen sizes
- Consistent card styling applied
### UI Improvements & Peer Feedback Implementation

#### Centered Footer (Xadrian’s Suggestion)
The footer layout was updated to improve visual balance and alignment with the page structure.  
- The footer content is now centered using CSS (`text-align: center`).
- Padding and consistent spacing were added to match the header and main content areas.
- A top border was introduced to clearly separate the footer from the main content.

This change improves readability and creates a more cohesive layout across the page.

---

#### Footer on Each Page (Brandon’s Suggestion)
A consistent footer was implemented across all pages of the site to provide a unified user experience.

- A simplified footer was added to secondary pages (`events.html`, `locations.html`, `about.html`).
- The homepage retains a more detailed footer with additional informational content.
- All footers share the same styling (`.site-footer`) to maintain consistency.

This ensures all pages include clear site identity and navigation context.

---

##### Favicon Implementation
A custom favicon was added to enhance branding and improve browser tab recognition.

- A Font Awesome icon (`book-open-reader`) was exported as an SVG file and used for the favicon.
- The favicon is linked in each page’s `<head>` section:

```
<link rel="icon" href="images/Favicon.svg">
```
---
#### Adding Google Fonts 

Google Fonts allows custom fonts to be used on a website by loading them from Google's servers and applying them through CSS.

You only need two steps:
1) Add the font link in HTML
2) Use font-family in CSS

---

Add this to the <head> of every HTML page:
```
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Audiowide&family=Montserrat:ital,wght@0,100..900;1,100..900&family=Syncopate:wght@400;700&display=swap" rel="stylesheet">
```
Make sure your stylesheet is also linked:
```
<link rel="stylesheet" href="styles.css">
```
---

Apply fonts in your CSS file:

body {
  font-family: "Montserrat", sans-serif;
}

h1 {
  font-family: "Audiowide", sans-serif;
}

h2 {
  font-family: "Syncopate", sans-serif;
}

---

Optional: control thickness (weight)

h1 {
  font-weight: 700;
}

h2 {
  font-weight: 400;
}

---

IMPORTANT:

Google may show something like this:

.montserrat-<uniquifier> {
  font-family: "Montserrat", sans-serif;
  font-weight: <weight>;
}

Ignore it.

It is only a template. Do not copy it.

Instead, always apply fonts directly to elements like h1, h2, or body.

---

Rules:

- Font names must match exactly ("Montserrat", etc.)
- Always include a fallback (sans-serif, serif)
- Fonts are applied in CSS, not HTML
- One stylesheet controls the whole site

---

Working example:

```
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Audiowide&family=Montserrat:ital,wght@0,100..900;1,100..900&family=Syncopate:wght@400;700&display=swap" rel="stylesheet">
```
```
h1, h2 {
  font-family: "Montserrat", sans-serif;
}
```
---
### Custom Calendar UI (Card-Based Design)

This calendar transforms a basic HTML table into an interactive UI component using CSS cards, hover effects, and theme variables. The goal is to maintain a stable grid layout while making each day visually consistent and ready for interaction.

---

#### 1. Base Calendar Structure

The calendar uses a standard HTML table for layout:

    <table class="calendar">
      <thead>
        <tr>
          <th>Sun</th><th>Mon</th><th>Tue</th><th>Wed</th>
          <th>Thu</th><th>Fri</th><th>Sat</th>
        </tr>
      </thead>

      <tbody>
        <tr>
          <td></td>

          <td>
            <a href="#" class="day-card">
              <span class="day-number">1</span>
            </a>
          </td>

          <td>
            <a href="#" class="day-card">
              <span class="day-number">2</span>
            </a>
          </td>

          <td>
            <a href="event-meeting.html" class="day-card">
              <span class="day-number">11</span>
              <span class="event-label">Meeting</span>
            </a>
          </td>
        </tr>
      </tbody>
    </table>

---

### 2. Fix Uneven Calendar Rows

Originally, event text caused rows to stretch unevenly.

**Fix: Force equal cell sizing**

    .calendar {
      border-collapse: collapse;
      width: 100%;
      max-width: 600px;
      margin: auto;
      text-align: center;
    }

    .calendar td,
    .calendar th {
      width: 14.28%;
      height: 90px;
      border: 1px solid #ccc;
      vertical-align: top;
    }

This keeps all rows evenly aligned.

---

### 3. Convert Each Day into a Card

Each day is wrapped in a `.day-card` to create a structured layout:

    .day-card {
      display: flex;
      flex-direction: column;
      justify-content: space-between;

      height: 100%;
      padding: 6px;
      border-radius: 6px;

      text-decoration: none;
      color: inherit;
    }

**Benefits**

- Prevents layout distortion  
- Keeps all days visually consistent  
- Enables future interactivity  

---

### 4. Add Hover Interaction

Provide visual feedback on interaction:

    .day-card:hover {
      background-color: var(--accent);
      color: #fff;
    }

---

### 5. Wrap Calendar in a Card Container

Instead of styling the table directly, wrap it in a container:

    <div class="calendar-card">
      <table class="calendar">
        ...
      </table>
    </div>

    .calendar-card {
      max-width: 650px;
      margin: 1.5rem auto;
      padding: 1rem;

      border-radius: 10px;
      background: #ffffff;

      box-shadow: 0 8px 20px rgba(0, 0, 0, 0.08);
    }

    .calendar {
      background: transparent;
    }

---

### 6. Theme Integration

Update the dark theme accent color:

    [data-theme="dark"] {
      --accent: #6b1f1f;
    }

All hover effects automatically update because they use `var(--accent)`.

---

#### Final Result

- Stable table layout  
- Evenly sized cells  
- Card-style days  
- Hover interaction  
- Theme-aware styling  
- Clickable dates  

---

#### Key Concept

- Table → layout structure  
- Card → interactive component  

Each day becomes a reusable UI element inside a stable grid.