[Back](README.MD)
# CSS THE BOX MODEL
[samples html](html/css_box_model.html)

## The Inline elements, styles by default
[help](https://developer.mozilla.org/en-US/docs/Web/HTML/Inline_elements)
* Are made for final content, text or images
* Will take only the required horizontal and vertical space, you can never give with or height
* Respect left & right margins and padding, but not top & bottom
* You can apply top and bottom padding and border, but they could collide with other content [help](https://hacks.mozilla.org/2015/03/understanding-inline-box-model/)
* Will take the whitespaces between elements in the HTML into account!!

## The Block elements, styles by default
[help](https://developer.mozilla.org/es/docs/Web/HTML/Block-level_elements)
* Are usually made as containers of other elements
* Will take all the remaining horizontal space inside the parent element if with is not defined
* Respect all the margins and paddings
* Force a line break between elements

## Special scenario, the inline-block elements, just with custom styles
* Allow other elements to sit to their left and right (as inline)
* Respect top & bottom margins and padding (as block)
* Respect height and width (as block)
* Take the whitespaces between elements in account (as inline)

## Building the box

### The content
The content of the box, where text and images appear

### The padding
Clears an area around the content. The padding is transparent

### The border
A border that goes around the padding and content

### The margin
Clears an area outside the border. The margin is transparent
### The outline, ans special case

## Where is my margin?!!!

> The vertical margin of a block element will overlap with others of the same type. It will happen even with elements inside other containers.  
The larger margin between both will be applied.  
This behaviour help us to maintain consistency on our layout.  
There are ways to force margins to be cleared:
* Adding a border to the parent
* Adding a margin to the parent
* Making the parent as inline-block
