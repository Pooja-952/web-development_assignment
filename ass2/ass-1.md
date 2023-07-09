// Q.1 What’s Box Model in CSS ?

//Solution--->

The box model is a foundational concept in CSS that outlines the rendering of elements within a web page. It describes the structure and layout by envisioning elements as boxes comprising content, padding, borders, and margins.

CSS encompasses several properties associated with the box model, including:

Width and Height: These properties determine the dimensions of an element's content area. Padding: The padding property sets the space between an element's content and its border. It can be adjusted individually for the top, right, bottom, and left sides. Border: This property defines the appearance of an element's border, allowing customization of its style, thickness, and color. Margin: The margin property creates space around an element, establishing a gap between adjacent elements. Similar to padding, it can be specified for each side—top, right, bottom, and left.

**Q.2 What are the Different Types of Selectors in CSS & what are the advantages of them?**

Solution--->

CSS selectors are used to target and style specific HTML elements. Main types of selectors:

Type Selectors: Target elements based on their tag name (e.g., h1, p, div). They are simple and easy to use.

Class Selectors: Target elements with a specific class attribute value (e.g., .my-class). They promote modularity and reusability.

ID Selectors: Target a unique element with a specific ID attribute value (e.g., #my-id). They provide high specificity for individual styling or JavaScript interactions.

Attribute Selectors: Target elements based on their attribute values (e.g., [type="text"], [href^="https://"]). They offer flexibility in selecting elements that meet specific criteria.

Descendant Selectors: Target elements that are descendants of another element (e.g., div p, ul li). They help style specific elements within nested structures.

Pseudo-classes and Pseudo-elements: Target elements based on states or specific parts (e.g., :hover, :nth-child(2), ::before). They provide dynamic styling and additional effects.

Advantages of using these selectors include specificity for precise targeting, reusability for consistent styles, flexibility in selecting elements, and readability for maintainability.

# Q.3 What is VW/VH ?

//Solution--->

Viewport Units (VW/VH):

VW (viewport width) represents a percentage of the width of the viewport, while VH (viewport height) represents a percentage of the viewport's height.
These units are relative to the size of the viewport, allowing for responsive designs that adapt to different screen sizes.
For example, 1vw is equal to 1% of the viewport width, and 1vh is equal to 1% of the viewport height.
When elements are sized using VW/VH units, their dimensions adjust dynamically as the viewport size changes.
An example usage is setting an element's width to 50vw, which makes it occupy 50% of the viewport width.
Pixels (px):

Pixels are absolute units of measurement based on the screen resolution.
Each pixel represents one physical dot on the screen.
Pixel values are fixed and do not change with the size of the viewport.
Elements sized using pixels will maintain the same size regardless of the screen size.
Setting an element's width to 50px will make it 50 pixels wide, irrespective of the viewport's dimensions.

**Q.4 Whats difference between Inline, Inline Block and block ?**

//Solution--->

The display types inline, inline-block, and block determine how elements are shown and interact with other elements in a document. Here's a summary of each type:

Inline:

Flows within text content, doesn't start on a new line.
Takes up only necessary space for its content.
Examples: , , , .
No width, height properties. Margins, paddings, borders affect only horizontal space.
No line breaks before or after. Can align text vertically.
Inline-block:

Similar to inline, but behaves like block-level elements.
Flows within text content, can have width, height properties.
Respects margins, paddings, borders.
Examples: , , .
No line breaks before or after, unless additional content on the same line.
Block:

Starts on a new line, takes up the full available width.
Creates a block-level box.

**Q.5 How is Border-box different from Content Box?**

//Solution--->

The main difference between the border-box and content-box models is how they calculate the total size of an element, including its content, padding, and border.

1. border-box:
   - In the border-box model, the total size of an element is calculated by including the content width/height, padding, and border within the specified width and height.
   - This means that the padding and border are included within the specified width and height, and they do not increase the overall dimensions of the element.
   - The content area is calculated as width - (padding + border), and the total element size includes the content, padding, and border.

2. content-box:
   - The content-box model, which is the default, calculates the total size of an element by considering only the content width/height and not including padding and border.
   - In this model, the specified width and height represent only the content area, and any padding or border is added to the overall dimensions of the element.
   - The content area is calculated as the specified width and height, and the total element size includes the content, padding, and border.

   **Q.6 What’s z-index and How does it Function ?**

//Solution--->

In CSS, the z-index property is used to control the stacking order of positioned elements on a webpage. It specifies the order in which elements are stacked or layered on top of each other along the z-axis, which is perpendicular to the screen.
The z-index property accepts integer values and determines the priority of an element in relation to other elements. Elements with a higher z-index value will appear in front of elements with a lower value.
Example:
div {
  position: relative;
  z-index: 2;
}

p {
  position: relative;
  z-index: 1;
}

In this example, the div element will be stacked above the p element because it has a higher z-index value. 
If two elements have the same z-index value, the stacking order will depend on their position in the HTML markup.
Additionally, the z-index property only applies within the stacking context of its parent element. If an element is contained within another element with a different stacking context, the z-index values of the parent elements will determine the stacking order.

**Q.7 What’s Grid & Flex and difference between them?**

//Solution--->

Both Grid and Flexbox are CSS layout systems that allow us to create responsive and flexible web layouts.

1. Flexbox:
   - Flexbox (Flexible Box Layout) is designed for one-dimensional layouts, either in a row or a column.
   - It provides a flexible way to distribute space among items within a container, making it ideal for creating responsive designs, aligning items, and controlling their order.
   - Flexbox focuses on arranging items along a single axis, either horizontally (in a row) or vertically (in a column).
   - It allows us to control the size, alignment, and order of the flex items using properties like flex-direction, justify-content, align-items, and order.

2. Grid:
   - CSS Grid Layout is designed for two-dimensional layouts with rows and columns.
   - It provides a powerful grid-based layout system that allows us to define both the overall grid structure and the placement of items within the grid.
   - Grid allows us to create complex layouts with precise control over rows, columns, and the placement of items.
   - It enables us to define grid tracks, set their sizes, and position items in specific cells or areas using properties like  grid-template-columns ,  grid-template-rows ,  grid-column , and  grid-row .

Differences -
1. Grid and Flexbox differ in their dimensionality. Flexbox is a one-dimensional layout system, while Grid is two-dimensional, with rows and columns.
2. Flexbox focuses on arranging items along a single axis, while Grid provides more comprehensive control over both rows and columns, allowing for complex grid-based layouts.
3. Grid offers greater control over the overall grid structure, including item size and placement, while Flexbox emphasizes flexible item distribution within a single axis.
4. Both Grid and Flexbox can be used to create responsive layouts, but Flexbox is typically suitable for smaller-scale designs or for managing alignment and ordering within Grid layouts.
5. Flexbox enjoys better browser support overall, including compatibility with older versions, while Grid may have slightly limited support in older browsers but is well-supported in modern ones.

**Q.8 Difference between absolute and relative and sticky and fixed position explain with example.**

//Solution--->

1. Absolute Position:
   When an element is set to absolute position, it is positioned relative to its nearest positioned ancestor. If there is no positioned ancestor, it is positioned relative to the initial containing block (the browser window). The element is then taken out of the normal flow of the document, meaning other elements will not be affected by its position.

Example:
html

<style>
  .container {
    position: relative;
    height: 200px;
    width: 200px;
  }

  .absolute-box {
    position: absolute;
    top: 50px;
    left: 50px;
    height: 100px;
    width: 100px;
    background-color: red;
  }
</style>

<div class="container">
  <div class="absolute-box"></div>
</div>

In this example, the .absolute-box element is positioned absolutely relative to its .container ancestor. It is offset 50 pixels from the top and left edges of the container.

2. Relative Position:
   Relative position is similar to absolute position in that it allows you to position an element relative to its normal position. However, unlike absolute position, the element still occupies space in the normal flow of the document. Other elements will be positioned as if the element were still in its original position.

Example:
html

<style>
  .relative-box {
    position: relative;
    top: 50px;
    left: 50px;
    height: 100px;
    width: 100px;
    background-color: blue;
  }
</style>

<div class="relative-box"></div>

In this example, the .relative-box element is positioned relatively by offsetting it 50 pixels from the top and left edges of its original position.

3. Sticky Position:
   Sticky position is a hybrid of both relative and fixed positions. When an element is set to sticky, it behaves like a relatively positioned element until the user scrolls to a specific threshold. At that point, it becomes fixed relative to its nearest scrolling ancestor or the viewport if there is no scrolling ancestor.

Example:
html

<style>
  .sticky-box {
    position: sticky;
    top: 50px;
    height: 100px;
    width: 100px;
    background-color: green;
  }
</style>

<div class="sticky-box"></div>

In this example, the .sticky-box element is initially positioned relative to its normal position. However, when the user scrolls the page and the box reaches the top position (50 pixels from the top of the viewport), it becomes fixed and sticks to that position as the user continues to scroll.

4. Fixed Position:
   Fixed position is similar to absolute position, but it is always positioned relative to the viewport, regardless of scrolling. The element is taken out of the normal flow of the document and stays in the same position even if the user scrolls the page.

Example:
html

<style>
  .fixed-box {
    position: fixed;
    top: 50px;
    right: 50px;
    height: 100px;
    width: 100px;
    background-color: yellow;
  }
</style>

<div class="fixed-box"></div>

In this example, the .fixed-box element is positioned fixed to the top-right corner of the screen, regardless of scrolling.

