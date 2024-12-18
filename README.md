# CSS Nerdery Challenge

> [!NOTE]
> If you would like to check the latest changes deployed, go to the following link, because changes that are being evaluated for this challenge are until commits pushed by **Friday, dec 13th**. 
> **Link**: https://css-nerdery-challenge-steven.vercel.app

#
Latest Changes: https://css-nerdery-challenge-steven.vercel.app

Friday Dec 16th, 2024 Changes: https://css-nerdery-challenge-coci9n7zz-steven-carcamo-ravns-projects.vercel.app/


## Feedback

Pixel perfect:
- 75% accurate
- Some colors are different as the design. e.g: Font color in the “Recently Used” cards title (App Project, Project: fitbit…)
- The “Recent Files” cards have a different spacing and placement as the design.
- The “Storage” cards have a different spacing and placement as the design.
- The “Storage” graph has a different size than the design.

Responsiveness test:
- The web looks good when shrinking the vertical dimension. The scroll is broken for the left panel. At least the left panel should have an independent scroll behavior.
- The page in large width looks great.
- Scroll behavior in =< 840px in the right panel works great.
- The “Recently Used” card content overflows on viewport width =< 400px
- Horizontal scroll on “Recent Files” and “Share with me” is great. Missing in the “Recently Used” section.

Technical feedback:
- the CSS files are well organized into directories like abstracts, base, components, and layout. This modular approach helps in maintaining and scaling the project.
- the class names follow a consistent naming convention that resembles the BEM (Block Element Modifier) methodology, which is good for readability and maintainability.
- The use of CSS variables in variables.css for colors and other properties is excellent. It promotes reusability and makes it easier to manage theme changes
- The usage of media queries would improve the responsiveness.
- While @import is used for modularity, it can have performance drawbacks as it can block rendering.
- Improve the semantic class names: Ensure that all class names are as semantic as possible. For example, instead of using generic names like square, use more descriptive names like icon-square if it represents an icon.
- Avoid being coupled to html in your css: Using CSS selectors that are tightly coupled to specific HTML tags, such as >li, can be problematic for several reasons:
    - Specificity: It ensures that styles are applied only to the intended elements, which can be useful in certain scenarios.
    - Reduced Flexibility: It makes the CSS less flexible and harder to reuse. If the HTML structure changes, the CSS will need to be updated accordingly.
    - Maintainability: It can make the CSS harder to maintain, especially in larger projects where the HTML structure might evolve over time.
    
From
 .grid-container__left-sidebar--navigation-list > li {
  /* styles */
}
 To
 .navigation-list__item {
  /* styles */
}