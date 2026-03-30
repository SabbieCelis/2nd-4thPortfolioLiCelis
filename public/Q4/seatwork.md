# Answers to guided questions

### *Step 1 (static vs relative)*
The relative positioning bases off of the static position. With its respective adjustments, it will cause the element to be adjusted away from its normal/static position.

### *Step 2 (Fixed)*
When scrolling or zooming in and out of the page, the footer will stay fixed in the same place. This means it will always stay in the same place regardless if the page is scrolled. Compared to relative positioning, fixed positioning behaves more strictly as it can still be seen in the viewport.

### *Step 3 (Absolute)*
The effect of the absolute positioning on the div with class content showed that (without the top and left adjustments,) it would adjust to not be under the nearest div and follows the position of div with class sidebar. What absolute position does is it follows the relative positioning of the element nearest to it (in this case it is the sidebar). Compared to the previous position that we used on footer, absolute position does not stay on the viewport when scrolled or zoomed in, meaning it does not behave as strictly as fix positioning.

### *Step 4 (Absolute and z-index)*
Notice appears on top of the content because of its z-index. The values of z-index depend on which number is higher. Meaning the higher the number, the element wiwll be on the top most layer. If we swap the index values, notice will then not be seen in the html, meaning that it is under .content.

## Challenge Questions
