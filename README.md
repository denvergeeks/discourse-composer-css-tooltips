discourse-composer-css-tooltips

<div data-ttext>Hover over me!
  <span data-ttip>This is the Tooltip Content!</span>
</div>

---

### USAGE
```
<div data-ttext>Hover over me!
  <span data-ttip>This is the Tooltip Content!</span>
</div>
```

### CODE
```
/* CSS Tool Tip, from https://www.w3schools.com/css/css_tooltip.asp */

/* Prevent cutting off Tooltips at edges of content body */
.topic-body .cooked {
  overflow: visible;
}

/* Tooltip Anchor Text Container */
div[data-ttext] {
  position: relative;
  display: inline-block;
  border-bottom: 1px dashed #ccc; /* dots under the anchor text */
}

/* Tooltip Content Container */
span[data-ttip] {
  visibility: hidden;
  width: 120px;
  background-color: black;
  color: #fff;
  text-align: center;
  padding: 5px 0;
  border-radius: 6px;
  position: absolute;
  z-index: 1;
  /* Position the Tooltip - Use half of the width (120/2 = 60), to center the tooltip */
  bottom: 100%;
  left: 50%;
  margin-left: -60px;
}

/* Show the Tooltip Content Container when you mouse over the Tooltip Anchor Text */
div[data-ttext]:hover {
  span[data-ttip] {
    visibility: visible;
  }
}
```
