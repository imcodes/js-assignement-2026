# Calculator UI — Assignment Instructions

## Goal

Recreate the calculator UI shown in `calculator/sample UI.png` (the iPhone
Calculator app) using **only HTML and CSS**.

At this stage you are **not** writing any JavaScript. Your only job is to
build the visual layout and make sure the HTML markup is structured in a
way that will make it easy to "wire up" with JavaScript later.

## Reference

Open `calculator/sample UI.png` and study it closely before you start.
Notice:

- A history/expression line (small, grey text) above the main result,
  e.g. `38,670÷50,000`
- A large result display below it, e.g. `0.7734`
- A 4-column grid of round buttons below the display
- Three button colors:
  - **Light grey** — `AC`, `+/-`, `%`
  - **Dark grey** — the digits `0-9` and `.`
  - **Orange** — `÷`, `×`, `-`, `+`, `=`
- The bottom-left button in the last row is a calculator/RPN icon button
  (you will replace this with a backspace <- this will be used to clear errors one digit at atime)

## Steps

1. **Create your files** inside the `calculator/` folder:
   - `index.html`
   - `style.css`

2. **Build the display area** at the top:
   - One container for the calculator screen.
   - Inside it, two separate elements: one for the small expression/history
     text, and one for the large current result. Keep these separate — do
     not combine them into a single element, since JavaScript will need to
     update them independently later.

3. **Build the button grid**:
   - Use a 4-column grid (CSS Grid is a good fit for this).
   - Each button should be its own `<button>` element — do not use `<div>`
     for buttons, since buttons are naturally clickable and keyboard
     accessible.
   - Give every button a `class` that identifies its color/role, for example:
     `class="btn btn-function"`, `class="btn btn-operator"`,
     `class="btn btn-digit"`.
   - Give every button a `data-value` attribute with the value it represents,
     for example: `<button class="btn btn-digit" data-value="7">7</button>`
     or `<button class="btn btn-operator" data-value="÷">÷</button>`.
     This is the hook JavaScript will use later — it should not need to read
     the button's text to know what it does.


4. **Style with CSS**:
   - Dark background for the whole page/calculator.
   - Buttons should be circular (or pill-shaped for the wide `0` button).
   - Match the three button colors and the text colors shown in the image.
   - Use a large, readable font for the result and a smaller, muted font
     for the expression line.
   - Add a `:hover` or `:active` state on buttons so they visually respond
     to clicks, even though nothing happens yet.

5. **Keep it responsive**:
   - The calculator should look correct on a phone-sized screen (roughly
     320–420px wide), similar to the reference image.

## What NOT to do

- Do not write any JavaScript or `<script>` tags yet.
- Do not hardcode the display to only ever show `0.7734` — that's just the
  sample state in the screenshot. Your display elements should simply be
  ready to be updated later; their starting content can be `0`.
- Don't skip the `data-value` attributes — without them, wiring up the
  calculator logic later will be much harder.

## Done when

- The page visually matches the sample image (colors, layout, spacing,
  rounded buttons, 4-column grid, wide `0` button).
- Every button is a real `<button>` element with a sensible `class` and a
  `data-value` attribute.
- The display has two clearly separate elements (expression + result).
- No JavaScript is used.
