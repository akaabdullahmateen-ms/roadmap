# Box model

When laying out a document, the browser's rendering engine represents each element as a rectangular box according to the standard **CSS basic box model**. CSS determines the size, position, and properties (color, background, border size, etc.) of these boxes.

Every box is composed of four parts (or _areas_), defined by their respectiv-e edges: the _content edge_, _padding edge_, _border edge_, and _margin edge_.

## Content area

The **content area**, bounded by the content edge, contains the "real" content of the element, such as text, an image, or a video player. Its dimensions are the _content width_ (or _content-box width_) and the _content height_ (or _content-box height_). It often has a background color or background image.

If the `box-sizing` property is set to `content-box` (default) and if the element is a block element, the content area's size can be explicitly defined with the `width`, `min-width`, `max-width`, `height`, `min-height`, and `max-height` properties.

## Padding area

The **padding area**, bounded by the padding edge, extends the content area to include the element's padding. Its dimensions are the _padding-box width_ and the _padding-box height_.

The thickness of the padding is determined by the `padding-top`, `padding-right`, `padding-bottom`, `padding-left`, and shorthand `padding` properties.

## Border area

The **border area**, bounded by the border edge, extends the padding area to include the element's borders. Its dimensions are the _border-box width_ and the _border-box height_.

The thickness of the borders are determined by the `border-width` and shorthand `border` properties. If the `box-sizing` property is set to `border-box`, the border area's size can be explicitly defined with the `width`, `min-width`, `max-width`, `height`, `min-height`, and `max-height` properties. When there is a background `background-color` or `background-image` set on a box, it extends to the outer edge of the border (i.e. extends underneath the border in z-ordering). This default behavior can be altered with the `background-clip` CSS property.

## Margin area

The **margin area**, bounded by the margin edge, extends the border area to include an empty area used to separate the element from its neighbors. Its dimensions are the _margin-box width_ and the _margin-box height_.

The size of the margin area is determined by the `margin-top`, `margin-right`, `margin-bottom`, `margin-left`, and shorthand `margin` properties. When _margin collapsing_ occurs, the margin area is not clearly defined since margins are shared between boxes.

Finally, note that for non-replaced inline elements, the amount of space taken up (the contribution to the height of the line) is determined by the `line-height` property, even though the borders and padding are still displayed around the content.
