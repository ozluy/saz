# saz
css3 cross browser mixins for SASS
#### useage
import in your SASS file as follows...
````
@import 'saz'
````

### available mixins

#### boxShadow
````
.example-boxShadow{
  @include boxShadow(1px 1px 1px 1px #999);
}
````
creates
````
.example-boxShadow {
  -webkit-box-shadow: 1px 1px 1px 1px #999;
  -moz-box-shadow: 1px 1px 1px 1px #999;
  box-shadow: 1px 1px 1px 1px #999;
}
````
#### boxSizing
````
.example-boxSizing{
  @include boxSizing(border-box);
}
````
creates
````
.example-boxSizing {
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
}
````
#### borderRadius
````
.example-borderRadius{
  @include borderRadius(1px 0 0 1px);
}
````
creates
````
.example-borderRadius {
  -webkit-border-radius: 1px 0 0 1px;
  border-radius: 1px 0 0 1px;
}

````
#### transition
````
.example-transition{
  @include transition(all 400ms ease-in);
}
````
creates
````
.example-transition {
  -webkit-transition: all 400ms ease-in;
  -moz-transition: all 400ms ease-in;
  -ms-transition: all 400ms ease-in;
  -o-transition: all 400ms ease-in;
  transition: all 400ms ease-in;
}
````
#### multipleColomns
````
.example-multipleColomns{
  @include multipleColomns(4, 15px);
}
````
creates
````
.example-multipleColomns {
  -moz-column-count: 4;
  -moz-column-gap: 15px;
  -webkit-column-count: 4;
  -webkit-column-gap: 15px;
  column-count: 4;
  column-gap: 15px;
}

````
#### transform
````
.example-transform{
  @include transform(scale(2) translateX(270px));
}
````
creates
````
.example-transform {
  -moz-transform: scale(2) translateX(270px);
  -webkit-transform: scale(2) translateX(270px);
  -o-transform: scale(2) translateX(270px);
  -ms-transform: scale(2) translateX(270px);
  transform: scale(2) translateX(270px);
}
````
#### calc
````
.example-calc{
  @include calc(width, '100% - 30px');
}
````
creates
````
.example-calc {
  width: -webkit-calc(100% - 30px);
  width: -moz-calc(100% - 30px);
  width: calc(100% - 30px);
}
````
#### outline
````
.example-outline{
  @include outline('2px dotted #2', 5px);
}
````
creates
````
.example-outline {
  outline: "2px dotted #2";
  outline-offset: 5px;
}
````
#### fontFace
fontFace($name, $path, $weight: null, $style: null, $exts: eot woff2 woff ttf svg)
- $name(required)
- $path(required)
- $weight(optional)
- $style(optional)
- $exts(required: a list of file extensions)
````
 @include fontFace("Awesome Font", "../fonts/awesome-font.ttf",400 ,normal , eot woff2 woff ttf svg);

````
creates
````
@font-face {
  font-family: "Awesome Font";
  font-style: normal;
  font-weight: 400;
  src: url("../fonts/awesome-font.ttf.eot?") format("eot"), 
  url("../fonts/awesome-font.ttf.woff2") format("woff2"), 
  url("../fonts/awesome-font.ttf.woff") format("woff"), 
  url("../fonts/awesome-font.ttf.ttf") format("truetype"), 
  url("../fonts/awesome-font.ttf.svg#Awesome_Font") format("svg");
}

````


