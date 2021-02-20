This pure html and css web page is mainly focus on css box model and layout.

## Padding & Margin
Padding creates extra space within an element, while margin creates extra space around an element.
### Padding
```
padding: value; /*all side*/
padding: valueA valueB; /*top-bottom left-right*/
padding: valueA valueB valueC valueD; /*top right bottom left*/
```
### Margin
```
margin: value; /*all side*/
margin: valueA valueB; /*top-bottom left-right*/
margin: valueA valueB valueC valueD; /*top right bottom left*/
```
### margin: auto
```
margin: auto;
```
horizontally center the element within its container.
The element will then take up the specified width, and the remaining space will be split equally between the left and right margins.
**Note**: Center aligning has no effect if the width property is not set (or set to 100%).

## Display
```
display: none/block/inline/inline-block;
```
- none: make the element invisible
- inline: Displays an element as an inline element. Any height and width properties will have no effect
- block: Displays an element as an inline-level block container. The element itself is formatted as an inline element, but you can apply height and width values
- inline-block; Displays an element as a block element. It starts on a new line, and takes up the whole width

## Float
specifies how an element should float.
**Disadvantages**: Floating elements are tied to the document flow, which may harm the flexibility.
```
float: left/right/none;
```
- none: he element does not float. This is default
- left: The element floats to the left of its container
- right: The element floats to the right of its container
### clearfix
The clearfix class is used on a container of which all the children are floating. If you would not use this, the container would not get any height.
```
<html>
<head>
<style>
.content {
    background-color:red;
}
.left {
    float:left;
}
.right{
    float:right ;
}
.clearfix:after{
    display:block;
    clear:both;
    content:'';
}
</style>
</head>
<body>
    <div class="content clearfix">
        <div class="left">
            <p>Content1</p>
        </div>
        <div class="right">
            <p>Content2</p>
        </div>
    </div>
</body>
</html>
```
In this example, if "clearfix" isn't used, red background can't be applied.