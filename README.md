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

### ✅ Padding and/or margins on 3+ elements (aesthetic spacing)
- **Header padding** creates breathing room: `header { padding: 2rem 1.5rem; }`   
- **Main padding** creates gutters: `main { padding: 2rem 1.5rem; }`   
- **Card padding + spacing**: `.content-box { padding: 1.5rem; margin-bottom: 2rem; }`   
- **Row spacing**: `.about-layout { margin-bottom: 2rem; }`   

### ✅ Borders on at least one element
- Borders applied to every card for clear separation:
  - `.content-box { border: 0.1rem solid #e3e1db; }`   

### ✅ Background gradient (doesn’t harm readability)
- Background gradient is applied to the whole page:
  - `body { background: linear-gradient(...); }`   
- Readability stays high because text sits on white `.content-box` cards:
  - `.content-box { background-color: #ffffff; }`   

### ✅ 2nd page uses a 2‑column layout
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

## DevTools / Inspector: the debugging move I should use next time
If columns stack unexpectedly, the fastest checks are:

1. Inspect `.about-image` (or `.about-history`) → confirm `float: left` is applied.   
2. Look at the **box model** panel → see content size vs padding vs border (why it doesn’t fit).   
3. Inspect `main` → confirm it has `max-width: 900px` and padding (container constraints).   
4. Inspect `.about-layout` → confirm `overflow: hidden` (row clearing).   

---

## Future checklist (what I should remember)
- ✅ Always group columns into row wrappers (`.about-layout`).   
- ✅ Floats need: `float + width + gap`, plus a clear (`overflow: hidden`).   
- ✅ Container width matters (`main max-width`).   
- ✅ Padding/border are part of layout reality (they can cause stacking).   
- ✅ Always include a mobile stack fallback.   

---
# 📚 3D Carousel (CSS-Only) — Featured Reads

## Overview

This feature implements a **3D rotating carousel** that displays five fictional book titles using **pure HTML and CSS (no JavaScript)**.

The carousel appears on the **Home page** under *Featured Reads*, providing a visual introduction to the types of books explored by the FictionTown Book Club.

---

## 🧠 Design Intent

The carousel is intentionally placed within the page flow:

Welcome → Featured Reads (visual) → Upcoming Highlights → Community

- **Welcome** introduces the club  
- **Carousel** shows what the club reads  
- **Highlights** provide structured information  
- **Community section** adds emotional context  

This approach balances visual interest with readability.

---

## ⚙️ How It Works

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

## ♿ Accessibility Consideration

Motion can be reduced for users who prefer it:

    @media (prefers-reduced-motion: reduce) {
      .carousel {
        animation: none;
      }
    }

- This improves accessibility and usability

---

## 🎨 Visual Design Choices

- Soft background (`#faf8f4`) → calm reading aesthetic  
- Serif font (Georgia) → literary tone  
- Subtle shadows → gentle depth  

The goal was to keep the effect **clean and readable**, not distracting.

---

## ✅ Constraints & Decisions
  
- ✅ CSS-only animation used  
- ✅ Semantic HTML maintained  


---

## 🚀 Key Takeaways

This feature demonstrates:

- CSS 3D transforms (`rotateY`, `translateZ`)
- Animation with `@keyframes`
- Depth using `perspective`
- Structured layout integration
- Accessibility awareness

---

## 🧩 Reflection

This component reinforces an important idea:

Structure enables creativity.

By organizing the page first, the carousel could be added as a purposeful visual element rather than a distraction.