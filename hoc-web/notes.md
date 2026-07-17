alt + arrow
shift + alt
choose many class/tags, then press F1->wrap with abbreviation->create father elements(capable create class also); could be nesting many tags
reset css
normalize css-> default(standard start/begin)
font scale-> type scale
font awsome cdn
font awe some icon
google font-> choose font-> get font
https://developer.mozilla.org/en-US/
em(emphasis) better italic; strong better b

<h1>Xin chào</h1>
->Đây là tiêu đề lớn nhất/quan trọng nhất
html describes:"what content is this" not "what does it look like"
h1: main heading
p: paragraph
web browser automatically: makes context big; bold; emphasize
->semantic HTML(HTML mang ý nghĩa nội dung)
non-semantic HTML: <div>
parser
web browser deafault: makes heading bigger; paragraph smaller.
HTML: HyperText Markup Language
->A Language that MAKES structure of website
html is not programming language. 'Cause HTML:
-no calculating
-no thinking
-no progress/handle logic
HTML does DESCRIBE structure of content
web browser is developed to understand:
h1: big heading
p: paragraph
img: image
a: anchor/link
HTML: "quy ước chung"
hr: horzontal line -> block element
br, hr: void elements
heading organizes content
ul,ol = block
li = list item
ul>li>ul>li-> nested list
ul/ol default has padding 40-> li thụt vào
<ol type="A / a / i / I">
ol>li*5{text $$}
img src="cat.jpg alt="Mèo" ->src= source; alt = alternative text =>attribute of img
img: inline element; void element
<p>Hello</p>: Hello ->children content
img has visual content = rendering
tag xác định: bản chất/vai trò element
attribute: bổ sung info/behavior for tag
table
tr = table row (1 row)
td = table data (data of cell) ->display: table cell
tbody: table-row-group
th = table heading ->bold, justify, stronger semantic text for table(semantic structure)
table = data structure that organized
div = block element
span = inline element
text = inline content
input = void element
<input type="text" placeholder = "content">: input only 1 row->keep layout stable ; ->single-line form control
label + form structure
<form>
        <label>
        <input>/<area>
        <button>
</form>
inline elements can't have block ones into
inline elements can't have padding-top + bottom
inline elements can't have margin-top + bottom
inline elements can't have width, height, min-width, min-height
header, nav, main, section, footer = block element-> semantic
CSS: -> property: value -> color: red;
style="property 1: value; property 2: value;"
semi-colon(;) = end of declaration
content too large->overflow
ID-> don't use for CSS, just use for javascript
negative width/height->invalid->default auto
width: -100px; height: -800px; ->auto
screen coordinate system-> top-left
(0,0) ─────────→ +X
  │
  │
  │
  ↓
 +Y
 hover; active-> ~click
 element written first-> paint first
 element written second-> paint overlap relates to stacking
 z-index-> layer index
 position: relative-> still staying normal flow(keep place in layout)-> position of itself. 
 view of relative: [Box1]_____ [Box2][Box3]; but layout:[Box1][Box2][Box3]
 position: absolute/fixed-> real move and replaced by others-> position of 0,0(or nearest father's position) -> not occupy in layout
 white-space: wrap / nowrap
 a target = "_blank" href=https://......
 <a href = "tel:09123456">Call me</a>
 <a href = "mailto:abc@gmail.com">Call me</a>
 <blockquote>
 <img width="100%" src="" alt="">
 pre(preformatted)
 code
 &lt;-> < ; &gt;-> >
 &nbsp; ->non-breaking space
 code beautify-> translate code ->html escape
highlight code by prismJS:
<html>
...<head>
        <link rel="stylesheet"
      href="https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/themes/prism-tomorrow.min.css" />
</head>
<body>
<pre><code class="language-html/css/javascript..."> </code></pre>
...
        <script src="https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/prism.min.js"></script>
        <script src="https://cdnjs.cloudflare.com/ajax/libs/prism/1.29.0/components/prism-javascript.min.js"></script>
</body>
</html>

display: flex -> justify-content (horizon) & align-items(vertical)
display: flex;
flex-direction: column / row (reverse)
flex-wrap: wrap; nowrap(default)
align-items: ->flex container stretch(default); flex-start; flex-end; center; baseline; first-baseline; last-baseline;
align-content: use for many lines(>=2)
justify-content: center; space-around; space-evenly; space-between;
flex-start; flex-end
align-self-> flex items stronger/override align-items
justify-items-> only for GRID
gap: 100px ->space split ->container manages
margin->spacing of each item-self
flex-grow: make wide larger, ratio space child use. (default = 0)
flex-shrink: make wide less(devide), if = 0-> no change, only use for child (default = 1)
flex-basis:
grow case:(abundan 400px) 1,3,2-> total: 1 + 3 + 2 = 6->400/6 = 66.67
result: no.1: 100(flex-basis) + 66.67 = 166.67
no.2: 200(flex-basis) + 66.67*3 = 200 + 200 = 400
no.3: 100(flex-basis) + 66.67*2 = 100 + 133.34 = 233.34
flex: 1 1 100px;-> flex-grow: 1, flex-shrink: 1, flex-basis: 100px
flex: 2;-> flex-grow: 2; flex-shrink: 2; flex-basis: 0;
flexbox create rows/columns
display: grid
grid-template-columns: 100px 200px 300px; -> first column-100px; ...300px;
grid-template-rows: 50px 150px;-> first row-50px; second row-150px
grid create permanent cells
elements' size prior/stronger/override grid's cells
if elements don't have width/height or both-> size depends/heritages on cells
size of track->cells of grid
fr->fraction ~ flex-grow but divide by ratio -> more responsive
grid-template-columns: 2fr 3fr 5fr; -> 2 + 3 + 5 = 10 parts
grid-template-columns: 200px 1fr 3fr 100px; container: 1000px
-> permanent: 200 + 100 = 300
-> còn lại: 1000 - 300 = 700
-> sum of fr: 1 + 3 = 4
-> 1 part = 700/4 = 175
-> result: 200px 175px 525px 100px
grid-column: 1 / 4 -> start column-line 1, end column-line 4 ->3 column-> 4 - 1 = 3-> merge horizontal cells;
grid-column: 3 = grid-column: 3 / span 1->place in 3rd cell of 3rd column
grid-row: 3 ~ grid-column: 3
grid-row: 1 / 3(3 - 1 = 2) = 1 / span 2(1 + 2 =3) -> merge vertical cells
Implicit rows(rows created when have no space/place to insert elements)-> height: auto;
grid-auto-rows: px -> use to create cells when not enough place (for container)
grid-auto-columns: px -> use to create cells when not enough place (for container)
grid-template-columns: repeat(4, 100px) = 100px 100px 100px 100px
grid-template-columns: repeat(2, 1fr) = 1fr 1fr = 2fr (2 columns)
grid-template-columns: repeat(2, 1fr) 2
= 1fr 1fr 2fr = 4fr-> create 2 columns with each occupy 1fr + 1 columns occupy 2fr = total 3 columns
grid-template-columns: minmax(a, b)-> min = a, max = b
minmax(100px, 300px)-> min = 100px, max: 120px-300px
->cannot 50px-400px
grid-template-columns:
minmax(150px, 1fr)
minmax(150px, 1fr)
minmax(150px, 1fr);
-> 3 columns
minmax(200px, 1fr) -> min = 200px, max = fr
repeat(auto-fit, minmax(150px, 1fr))
-> create max of columns as possible; each column with min = 150px and possible responsive to occupy full of row
repeat(auto-fit, minmax(150px, 1fr)) container>=1000px (html=3 elemnts)
->[box 1][box 2][box 3]
repeat(auto-fill, minmax(150px, 1fr)) container>=1000px (html=3 elemnts)
->[box 1][box 2][box 3] [ ] [ ] [ ]
create max of columns as possible; keep vacant columns

overflow(-x/y): hidden/scroll/auto
white-space: nowrap;-> create 3 dots (...)
text-ellipsis
margin changes layout->push other elements
transform: translate: translate(x/y)-> change the way of painting, not break layout
transform: scale(X/Y) (1.5 / 2...)
transform: rotate(45 / 90 ...deg)
transform-origin default: center
transform-origin: top left;
transition: transform 3s, ; 1000ms = 1s
-transition-property: transform, background, color, width,...
-transition-duration
-transition-timing-function: ease(default), linear, ease-in-out,...
-transition-delay
transition: transform 2s linear/ease-in/ease-out/ease-in-out
linear->stable speed; ease-> slow-fast-less until slow
ease-in->slow-fast >< ease-out
transition-> capability of elements(alway ready) not just action when hover
.class {transition 3s;} -> capaple to animate in 3s
.class:hover {transform scale (2)} ->when hover i'll scale
transition: transform 2s, background-color 2s;

# {transition: transform 1s 1s;}

{transition-property: transform;
transition-duration: 1s;
transition-delay: 1s; }
animation-name: move;
animation-duration: 2s;
@keyframes move {
from / 0% {transform: translateX() / scale() / rotate();}
} to / 100% {transform: translateX() / scale() scale() rotate(); }

@keyframes move {
from 0% {transform: translate() rotate() scale();}
to 100% {transform: translate() rotate() scale();}
}
animation-duration ~ transition-duration
interpolate
animation-interation-count: infinite;
animation-direction: alternate / reverse / alternate-reverse;
red-blue: alternate-> red<->blue<->red ; 0%(red) 50%(blue) 100%(red)
animation-fill-mode: none;->default
animation-delay: 2s;
animation-fill-mode: both;
animation-fill-mode: forwards / backwards
animation-delay + animation-fill-mode: backwards
animation: move 3s linear infinite;

pseudo classes
:first-child
:last-child
:last-of-type
:nth-child(n) even / odd / 3n +- 0->(n++) 1st time: n=0 2nd++
:nth-last-child(n)
:only-child

:first-of-type
:last-of-type
:nth-of-type
:nth-last-of-type(n)
:only-of-type

.box1 p:first-child, .box2 p:first-child{...}->p of box1 & p of box2

Adjacent Sibling Selector (+)
General Sibling Selector (~)
tag/.class/#:first-child -> must be: tag/.class/# AND first-child
tag/.class/# :first-child -> in tag/.class/# search all first-child elements

tag/class/#[attribute] {} https://www.w3schools.com/cssref/css_selectors.php

p:is(:nth-child(6n+1), :nth-child(6n+2), :nth-child(6n+3), :nth-child(6n+4), :nth-child(6n+5))
{
background: yellow;
font-size: 20px;
}

p:is( p:nth-child(5n + 2), p:nth-child(5n + 3)) {
color: red;
font-size: 30px;
}

.paragraph:not(:first-of-type) {
color: red;
}

.content p:not(:nth-child(3n+2)) {
background-color: purple;
}

tag/class/#[attribute~="text(string)"]

a[lang|=en-]

emmet:
ul>li{Item $@3}*53: Item 3-Item 55 (*53 element; 3-55, 55-3+1=53)
ul>li.list\*2>a[href="#!"]{Item $}:

<li class="letter"><a href="#!">Item 1</a></li>
<li class="letter"><a href="#!">Item 2</a></li>

p{text $@0}\*4

margin collapse: sibling->top & bottom(ngược chiều); parent-child->cùng chiều
to remove collapse:
float: left/right; position: absolute; display: inline-block/flex
outline: only 1 value for 4 dimension
outline-offset

margin-left/right: auto; -> one side or middle. only use for block/flex/grid elements(display). only use for horizon
margin negative
