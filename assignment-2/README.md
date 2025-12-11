# Assignment 2 - CSS Layouts

## File Organization
* **index.html**: The main HTML document containing the structure (a container div with 6 child divs representing boxes A through F).
* **styleA.css**: The stylesheet for "Version A". It uses CSS Flexbox (flex-direction: column) to align boxes vertically and `justify-content: space-evenly` to distribute them across the full height of the viewport.
* **styleB.css**: The stylesheet for "Version B". It uses `display: inline-block` along with `white-space: nowrap` on the container to keep the first five boxes in a horizontal line regardless of window width. The last box (F) is positioned using `position: fixed` to stay in the bottom-right corner.

## Challenges Faced
1.  **Vertical Spacing in Style A**: Achieving equal vertical spacing that responds to window resizing required setting the `html` and `body` height to 100% and using the Flexbox property `justify-content: space-evenly`.
2.  **Measurements in Style B**: Ensuring the total width remained 100px despite the 10px border and padding required the use of `box-sizing: border-box`.
3.  **Positioning Box F**: In Style B, keeping boxes A-E in the document flow while removing box F to the corner was solved by applying `position: fixed` only to the `:last-child`, which removes it from the flow and pins it relative to the viewport.