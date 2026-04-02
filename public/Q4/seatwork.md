# Seatwork No. 2 (CSS Position and z-index)

## Answers to Guided Questions

### *Step 1 (static vs relative)*
The relative positioning bases off of the static position. With its respective adjustments, it will cause the element to be adjusted away from its normal/static position.

### *Step 2 (Fixed)*
When scrolling or zooming in and out of the page, the footer will stay fixed in the same place. This means it will always stay in the same place regardless if the page is scrolled. Compared to relative positioning, fixed positioning behaves more strictly as it can still be seen in the viewport.

### *Step 3 (Absolute)*
The effect of the absolute positioning on the div with class content showed that (without the top and left adjustments,) it would adjust to not be under the nearest div and follows the position of div with class sidebar. What absolute position does is it follows the relative positioning of the element nearest to it (in this case it is the sidebar). Compared to the previous position that we used on footer, absolute position does not stay on the viewport when scrolled or zoomed in, meaning it does not behave as strictly as fix positioning.

### *Step 4 (Absolute and z-index)*
Notice appears on top of the content because of its z-index. The values of z-index depend on which number is higher. Meaning the higher the number, the element wiwll be on the top most layer. If we swap the index values, notice will then not be seen in the html, meaning that it is under .content.

## Challenge Questions

* The changes needed to be made in order to put our .notice box onto the top right corner of our .content box is by putting our div for notice into the div of our content box. For CSS fixes, the style for .notice will have all adjustments for top set to 0 and `left: 400px;` will be replaced with `right: 0;` .

### CSS Fixes:
```
.content {
    background: lightyellow;
    width: 300px;
    height: 200px;
    position: relative; top: -180px; left: 200px;
    z-index: 1;
}   
.notice {
    position: absolute;
    top: 0;
    right: 0;
    background: orange;
    padding: 10px;
    z-index: 2;
}
```
### HTML Fixes:
```
  <div class="content">Main Content
    <div class="notice">Notice!</div>
  </div>
```

* When .content has `position:relative`, it stay in its normal place in our layout, our top and left attributes only adjust the position it and our .notice stays anchored (since it is nested inside our content div). Meanwhile when we have `position:fixed` it will stay the same, but .content will be moved to another position. When we remove our .notice from the content div, it will float around the viewport.

* The .notice box appears above the .content box because of its higher z-index value (2 > 1). Z-index controls the stacking order of different elements, whereas elements with higher values are displayed infront of those with lower values.

# Reflection
1. To summarize, `position:static` is the default positioning for all HTML elements meaning it is placed according to document flow and it is the only position value that is not affected by the top bottom left right adjustments. `position:relative` is positioned *relative* to its static position and can be shifted using the top, left, right, bottom properties. `position:fixed` is positioned relative to the viewport or webpage, meaning it wwill stay on screen regardless of scrolling away. `position:absolute` is positioned based on the nearest positioned element (besides static), if no positioned ancestors are present, it is positioned relative to the viewport.

2. Absolute positioning depends on the nearest positioned ancestor (that is NOT static). If the parent element has its own position value other than static, then the element with `position:absolute` will be placed relative to that parent. If not, it will be placed relative to the viewport.

3. `position:sticky`is a combination of both relative and fixed positions. Before scrolling, it is positioned relative until it reaches a point where we scroll past it, it will then *stick* into that place just like `position:fixed`. 

    * Additional info that I wanna share for no. 3: `position:sticky` can actually be seen when viewing our github code files! When we scroll past the header, we would have `Preview | Code | Blame` and shows our file path (or where the file is located) sticked at the top of the viewport.

4. Positioning can be used to highlight important information by controlling where and when elements appear  on the webpage. An example of this can be the use of `position:sticky` for our navigation bar and/or `position:fixed` for our footer.