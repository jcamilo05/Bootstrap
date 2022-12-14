# This repo contains some useful information about Bootstrap 5 

## BREAKPOINTS

In bootstrap there are **6 default breakpoints**  

**Extra small: < 576px**  
**Small: >= 576px (sm)**  
**Medium: >= 768px (md)**
**Large: >= 992px (lg)**  
**Extra Large: >= 1200px (xl)**  

## Grid System

Bootstrap's grid system uses a series of containers, rows and columns to layout and align content.

### Columns

Bootstrap support until 12 columns, the column's number desired must be specified, otherwise this will be automatically adjust to the screen size.

**Equal width**  

To have columns with equal width just type col as a class, so for example the next chunk put 2 and 3 columns automatically.

```html
<div class="container border">
<h3 class="component-variation text-muted">Equal width</h3>
<p>Grid with auto-layout and equal width</p>
<div class="row">
<div class="col border">.col</div>
<div class="col border">.col</div>
</div>
<div class="row">
<div class="col border">.col</div>
<div class="col border">.col</div>
<div class="col border">.col</div>
</div>
</div>     
```

The previous code, look like the following image.


![](./img/notes/equalCol.JPG)


**One column width**

A column can be set with a predefined width, one can predefine how many columns set in a row, but taking in account that the max of columns is 12, so for example the following chunk of code set the second column with 7, and the others two columns are adjust automatically, all depend of screen size.

```html
<div class="row">
<div class="col border">.col</div>
<div class="col-7 border">.col-7</div>
<div class="col border">.col</div>
</div>

```
The previous chunk of code looks like the following image

![](./img/notes/setWidth.JPG)


**Responsive**  
The columns can be setted to resize depending on the size screen, so for example the following code set 3 different possible values, the first one when the device is small, and it put until 12 columns, the second one is setted for medium device what is setted until 6 columns, and the last one which is setted to large devices.

```html
<div class="row">
<div class="col-12 col-md-6 col-lg-3 border">.col-12 .col-md-6 .col-lg-3</div>
<div class="col-12 col-md-6 col-lg-3 border">.col-12 .col-md-6 .col-lg-3</div>
<div class="col-12 col-md-6 col-lg-3 border">.col-12 .col-md-6 .col-lg-3</div>
<div class="col-12 col-md-6 col-lg-3 border">.col-12 .col-md-6 .col-lg-3</div>
</div>

```
The previous setup put one column until 768px that is when a medium size begins, then it will have 2 columns until get 992px that is when the larger size is taken.

The following screenshots shows the previous paragraph.

#### small size (until 768px)


![](./img/notes/smallResp.JPG)

#### Medium size (until 992px)

![](./img/notes/mediumResp.JPG)

#### Large size (until 992px)

![](./img/notes/largeResp.JPG)

### CSS note

```css
div[class^="test"]{
background: #fff;
```
The meaning of the previous notation is set a background to all divs which have a class name of test

## Vertical alignments

The columns can be align horizontally with the following 3 tags.

```html
<div class="row align-items-start"></div>
<div class="row align-items-center"></div>
<div class="row align-items-end"></div>
```

The previous 3 alignments look like the following images

![](./img/notes/verticalAlig.JPG)

## Horizontal alignment

There are 6 different to set the horizontal alignment with Bootstrap

The following chunk, shows the 6 tags available to set the horizontal alignments and how it looks like..

```html
<div class="row justify-content-start"></div>
```
![](./img/notes/horizontal.JPG)


```html
<div class="row justify-content-center"></div>
```
![](./img/notes/center.JPG)

```html
<div class="row justify-content-end"></div>
```
![](./img/notes/end.JPG)

```html
<div class="row justify-content-around"></div>
```
![](./img/notes/around.JPG)

```html
<div class="row justify-content-between"></div>
```
![](./img/notes/between.JPG)

```html
<div class="row justify-content-evenly"></div>
```
![](./img/notes/evenly.JPG)

## Images

### Responsive images

Images in bootstrap are made responsive with  

``` html
<img class="img-fluid">
```

## Forms

The tag to create a form is `<form>` and inside this tag is put label and input, label has normally a **for** and a **class**, and input also has **class** but also a type, placeholder (which is the name inside the writing field, and) and id the following piece of code shows a small form who has two labels and two inputs.


```html
<form>
<fieldset>
<div class="mb-3">
<label for="inputEmail" class="form-label">Email input label</label>
<input type="email" class="form-control" placeholder="Email input placeholder" id="inputEmail">
</div>
<div class="mb-3">
<label for="inputPassword" class="form-label">Password input label</label>
<input type="email" class="form-control" placeholder="Password input placeholder" id="inputPassword">
</div>
<button type="submit" class="btn btn-primary">Submit</button>
</fieldset>
<form>
```
![](./img/notes/fieldset.JPG)

There is a way of place a text below the input box, this is useful to give information to the person who must fill up the form. Basically to add this helper you must write the attribute named `aria-describedby `  to the input, then add a `<p>` below with the id assigned to **aria-describedby**, the following example show that.


```html
<fieldset class="border">
<div class="mb-3">
<legend>Legend</legend>
<label for="inputTextStacked" class="form-label">Text input label</label>
<input type="text" class="form-control" placeholder="Text input placeholder" id="inputTextStacked" aria-describedby="inputTextStackedHelp">
<p id="inputTextStackedHelp" class="form-text">Here goes the helper to fill the input</p>
</div>
<div class="mb-3">
<label for="inputPassword" class="form-label">Password input label</label>
<input type="email" class="form-control" placeholder="Password input placeholder" id="inputPassword" aria-describedby="inputPasswordHelper">
<p id="" class="form-text">Here goes another helper but to the password</p>
</div>
<button type="submit" class="btn btn-primary">Submit</button>
</fieldset>

```

![](./img/notes/helper.png)


## Checks and radios

To create a radio is similar to create whatever form, its mean it must be typed input and label, but in **type** must be write "radio" and in **class** must be write form-check-input, the same applies to checkbox but in **type** must be write checkbox. The following example show us how to create a checkbox and a radio.

```html
<div class="form-check">
<input type="checkbox" class="form-check-input" id="checkDefault1">
<label class="form-check-label" for="checkDefault1">Default checkbox</label>
</div>

<div class="form-check">
<input type="radio" class="form-check-input" id="checkDefault2">
<label class="form-check-label" for="checkDefault2">Checked checkbox</label>
</div>

```
![](./img/notes/check.JPG)

# Components

## Accordion

Accordion is a collapsible that is used to hide or show things.

An accordion has is made up by basically two parts, the first one is a div with the accordion class `<div class=accordion>`, and the second part is the tag which contains the items `<div class=accordion-item>`; but the accordion item is divided by also two parts, the accordion header `<div class="accordion-header">` and the accordion body `<div class="accordion-body">`.

The following chunk of code shows one accordion.

```html
<div class="accordion" id="accordionDefault">
<div class="accordion-item">
<h2 class="accordion-header" id="headingDefaultOne">
<button type="button" class="accordion-button" data-bs-toggle="collapse" 
data-bs-target="#collapseDefaultOne" aria-expanded="true" aria-controls="collapseDefaultOne">
Accordion Item #1
</button>
</h2>
<div id="collapseDefaultOne" class="accordion-collapse collapse show" aria-labelledby="headingDefaultOne"
data-bs-parent="#accordionDefault">
<div class="accordion-body">
Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum a velit sodales, 
semper purus lacinia, venenatis diam. Sed erat sem, blandit ut purus id, ornare congue nunc. 
Fusce nunc purus, luctus id fermentum at, semper ut ligula
</div>
</div>
</div>

```
The following shows the previous code rendered

![](./img/notes/accordion.JPG)

## Buttons

Bootstrap have predefined the following 8 buttons
```html
<div class="code-example mb-5">
<h3 class="component-variation text-muted">Default</h3>
<div class="code-live">
<button type="button" class="btn btn-primary">Primary</button>
<button type="button" class="btn btn-secondary">Secondary</button>
<button type="button" class="btn btn-success">Success</button>
<button type="button" class="btn btn-danger">Danger</button>
<button type="button" class="btn btn-warning">Warning</button>
<button type="button" class="btn btn-info">Info</button>
<button type="button" class="btn btn-light">Light</button>
<button type="button" class="btn btn-dark">Dark</button>
</div>
</div>
```
The previous buttons looks like the following

![](./img/notes/button.JPG)

## Cards

Card is a flexible and extensible content container, a card is basically a container with differents types of cards atrtibutes, the following examples show some of the most basics cards.

### Basic card

The following card, is the most basic card, but has just a text inside it.

```html
<div class="card w-50">
<div class="card body">
<p class="card-text">
Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec ultricies sed velit ut
sollicitudin. In commodo, neque quis commodo scelerisque, urna nisi feugiat neque, et 
facilisis sem purus a dui. Maecenas tincidunt, elit ac sollicitudin dignissim, ex felis 
dictum ipsum, in imperdiet ipsum leo sollicitudin.
</p>
<p class="card-text">
Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec ultricies sed velit ut
sollicitudin. In commodo, neque quis commodo scelerisque, urna nisi feugiat neque, et 
facilisis sem purus a dui. Maecenas tincidunt, elit ac sollicitudin dignissim, ex felis 
dictum ipsum, in imperdiet ipsum leo sollicitudin.
</p>
</div>
</div

```

![](./img/card/basic.JPG)

### Card title and subtitle

As we see in the previous code, a card has a `card body` but inside card body, we can place a title and a subtitle,
the following chunks shows how it works.

```html
<div class="h5 text-muted mt-3">Title</h4>
<div class="card w-50">
<div class="card-body">
<h4 class="card-title">Card title</h4>
</div>
</div>
<h4 class="h5 text-muted mt-3">Subtitle</h4>
<div class="card w-50">
<div class="card-body">
<h6 class="card-subtitle">Card subtitle</h6> 
</div>
</div>
```

![](./img/card/title.JPG)

### Card Image top

To make a card with a top image, yo must place inside a card attribute a `<img>` with a class named **card-img-top**  and then place a normal card-body, and inside it can you place the attributes wished, like for example car-title, card-subtitle, card-text...

Teh following chunk of code shows a basic card image top.

```html
<div class="card w-50">
<img src="./img/card/400x200.png" alt="card image in the top" class="card-img-top">
<div class="card-body">
<div class="card-title">Card title</div> 
<div class="card-text">Lorem ipsum dolor sit amet, consectetur adipiscing elit. 
Donec ultricies sed velit ut sollicitudin. In commodo, neque quis commodo scelerisque, 
urna nisi feugiat neque, et facilisis sem purus a dui. Maecenas tincidunt, elit ac 
sollicitudin dignissim, ex felis dictum ipsum, in imperdiet ipsum leo sollicitudin.
</div>
</div>
</div>
```

![](./img/card/top.JPG)

### Card navigation

To create a nav navigation, inside a card must be typed a `class="card-header"` and a `class="card-body`, but inisde the class header is needed set a list item but with the following attribute, `nav nav-tabs card-header-tabs` must be placed inside `<ul>` tag, and inside each `<li>` must be placed `class="nav-item"`

The following chunk of code, shows the previously said.

```html
<div class="card w-50">
<div class="card-header">
<ul class="nav nav-tabs card-header-tabs">
<li class="nav-item">
<a href="#" class="nav-link active">Active</a>
</li>
<li class="nav-item">
<a href="#" class="nav-link">Link</a>
</li>
<li class="nav-item">
<a href="#" class="nav-link disable">Disable</a>
</li>
</ul>
</div>
<div class="card-body">
<h4 class="card-title">Card title</h4>
<p class="card-text">
Lorem ipsum dolor sit amet, consectetur adipiscing elit. 
Donec ultricies sed velit ut sollicitudin. In commodo, neque quis commodo 
scelerisque, urna nisi feugiat neque, et facilisis sem purus a dui. Maecenas tincidunt, 
elit ac sollicitudin dignissim, ex felis dictum ipsum, in imperdiet ipsum leo sollicitudin.
</p>
</div>
</div>
```
The previous code, looks like the following


![](./img/card/nav.JPG)

### Grid cards

Responsives cards can be created with grid system `class= row-cols-*-*`  the following code, shows a 4 responsive cards.

```html

<div class="code-live">
<h4 class="h5 text-muted mt-3">Default</h4>
<div class="row row-cols-1 row-cols-md-2 row-cols-xl-3 row-cols-xxl-4 g-4 mb-4">
<div class="col">
<img class="card-img-top" src="./img/card/300x150.png" alt="card image">
<div class="card-body">
<h4 class="card-title">Card title</h4>
<p class="card-text">
Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec ultricies sed 
velit ut sollicitudin. In commodo, neque quis commodo scelerisque, urna nisi 
feugiat neque, et facilisis sem purus a dui. Maecenas tincidunt, elit ac 
sollicitudin dignissim, ex felis dictum ipsum, in imperdiet ipsum leo sollicitudin.
</p>
</div>
</div>
<div class="col">
<img class="card-img-top" src="./img/card/300x150.png" alt="card image">
<div class="card-body">
<h4 class="card-title">Card title</h4>
<p class="card-text">
Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec ultricies sed 
velit ut sollicitudin. In commodo, neque quis commodo scelerisque, urna nisi 
feugiat neque, et facilisis sem purus a dui. Maecenas tincidunt, elit ac 
sollicitudin dignissim, ex felis dictum ipsum, in imperdiet ipsum leo sollicitudin.
</p>
</div>
</div>
<div class="col">
<img class="card-img-top" src="./img/card/300x150.png" alt="card image">
<div class="card-body">
<h4 class="card-title">Card title</h4>
<p class="card-text">
Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec ultricies sed 
velit ut sollicitudin. In commodo, neque quis commodo scelerisque, urna nisi 
feugiat neque, et facilisis sem purus a dui. Maecenas tincidunt, elit ac 
sollicitudin dignissim, ex felis dictum ipsum, in imperdiet ipsum leo sollicitudin.
</p>
</div>
</div>
<div class="col">
<img class="card-img-top" src="./img/card/300x150.png" alt="card image">
<div class="card-body">
<h4 class="card-title">Card title</h4>
<p class="card-text">
Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec ultricies sed 
velit ut sollicitudin. In commodo, neque quis commodo scelerisque, urna nisi 
feugiat neque, et facilisis sem purus a dui. Maecenas tincidunt, elit ac 
sollicitudin dignissim, ex felis dictum ipsum, in imperdiet ipsum leo sollicitudin.
</p>
</div>
</div>
</div>
</div>

```

### Small

![](./img/card/nav.JPG)

### Medium

![](./img/card/medium.JPG)

### Large

![](./img/card/large.JPG)

## Carousel

A carousel is made up basically of three tags, the firs one `class="carousel slide"` which is the most outer tag, inside the previous tag must be placed `class="carousel-inner"` and inside the last one, each slide must be tagged with a class called `class="carousel-item"`.One of the carousel inner must be placed with an atribute of the active, otherwise not carousel will be show.

The following is a carousel which also has indicators

```html
<div class="code-live">
<div id="carouselIndicators" class="carousel slide" data-bs-ride="carousel">
<div class="carousel-indicators">
<button type="button" data-bs-target="#carouselIndicators" data-bs-slide-to="0" class="active">
</button>
<button type="button" data-bs-target="#carouselIndicators" data-bs-slide-to="1"></button>
<button type="button" data-bs-target="#carouselIndicators" data-bs-slide-to="2"></button>
<button type="button" data-bs-target="#carouselIndicators" data-bs-slide-to="3"></button>
</div>
<div class="carousel-inner">
<div class="carousel-item active">
<img src="./img/carousel/1200x600-success.png" alt="First slide" class="d-block w-100">
</div>
<div class="carousel-item">
<img src="./img/carousel/1200x600-danger.png" alt="Second slide" class="d-block w-100">
</div>
<div class="carousel-item">
<img src="./img/carousel/1200x600-warning.png" alt="Third slide" class="d-block w-100">
</div>
<div class="carousel-item">
<img src="./img/carousel/1200x600-info.png" alt="Fourth slide" class="d-block w-100">
</div>
</div>
</div>
<button type="button" class="carousel-control-prev" data-bs-target="#carouselControls"
data-bs-slide="prev">
<span class="carousel-control-prev-icon" aria-hidden="true"></span>
<span class="visually-hidden">Previous</span>
</button>
<button type="button" class="carousel-control-next" data-bs-target="#carouselControls" data-bs-slide="next">
<span class="carousel-control-next-icon" aria-hidden="true"></span>
</button>
</div>
```

### Dropdown

A dropdown is like a list box that shows only one item when inactive. To create a dropdown, first it must be write a div with the class `class="dropdown"` and inside it, a dropdown  class called `class=dropdown-menu` and then inside each class, a class called dropdown-item `class=dropdown-item` 

The following chunk of code, shows a basic dropdown.

```html

<div class="dropdown ">
<button type="button" class="btn btn-secondary dropdown-toggle" id="dropdownButton" 
data-bs-toggle="dropdown" aria-expanded="false">Dropdown button</button>
<div class="dropdown-menu" aria-labelledby="dropdownButton">
<a href="#" class="dropdown-item">First item</a>
<a href="#" class="dropdown-item">Second item</a>
<a href="#" class="dropdown-item">Third item</a>
</div>
</div>
```
### Navs and tabs

A nav is horizontal menu, to create one there are two ways of doing that.

1. add `<class="nav"` to a nav element, followed by `<class="nav-link">` for each `<a>` tag
2. add `class="nav"` to a `<ul>` element, followed by `class="nav-item"` for each `<li>` and add `class="nav-link"`.

Whichever tags picked the result will be the same, the follwing chunk of code an image show the previous said

```html

<div class="code-live">
<ul class="nav">
<li class="nav-item">
<a href="#" class="nav-link active" aria-current="page">Active</a>
</li>
<li>
<a href="#" class="nav-link">Link</a>
</li>
<a href="#" class="nav-link disabled" tabindex="-1" aria-disabled="true">Disable</a>
</li>
</ul>
</div>
```
or 

```html
<div class="code-example mb-5">
<h3 class="component-variation text-muted">Links</h3>
<div class="code-live">
<nav class="nav">
<a href="#" class="nav-link active" aria-current="page">Active</a>
<a href="#" class="nav-link">Link</a>
<a href="#" class="nav-link disabled">Disable</a>
</nav>
</div>
</div>
```
![](./img/card/nav_tab.JPG)

## Navigation bar (Navbar)

A navigation bar is a navigation header that is placed at the top of the page.
The most basic navigation bar is made with a `<navi class=nav>` and inside it an unordered list with the class oh navbar-nav `<ul class=navbar-nav>`and in each list item a class of nav-item `<li class=nav-item>` and then inside each item an anchor tag with the class of nav-link `<a class=nav-link>`

The following chunk of code, shows how to create a basic navbar

```html
<nav class="navbar navbar-light bg-light navbar-expand">
<div class="container">
<a href="#" class="navbar-brand">Navbar</a>
<div class="collapse navbar-collapse">
<ul class="navbar-nav">
<li class="nav-item">
  <a href="#" class="nav-link active" aria-current="page">Active</a>
 </li>
<li class="nav-item">
  <a href="#" class="nav-link">Active</a>
 </li>
<li class="nav-item">
  <a href="#" class="nav-link">Link</a>
 </li>
<li class="nav-item">
  <a href="#" class="nav-link" tabindex="-1" aria-disable="true">Disable</a>
</li>
</ul>
</div>
</div>
</nav>
```

![](./img/nav/nav.JPG)

#### Navbar collapsable
Some times is useful to have a navbar which is raplaced by a button in small devices, to do so first must be created a nav with class navbar `<nav class="navbar">` then a div which must contain inside them the followngs tags.
`<button>` this tag must have as attribute `class="navbar-toggler"`, `data-bs-toggle="collapse"` and `data-bs-target=#AnIdName`and inside the button to create ten icon one the following span `<span class="navbar-toggler-icon"></span>`when the previous is done, must be typed a simple navbar but with the id name which was set in the data-bs-target.

The following chunk of code show a simple collapsable navbar

```html
<div class="navbar navbar-light bg-light navbar-expand-sm">
    <div class="container">
      <button type="button" class="navbar-toggler" data-bs-toggle="collapse"
      data-bs-target="#navbarResponsiveLeft" aria-controls="navbarResponsiveLeft">
        <span class="navbar-toggler-icon"></span>
      </button>
      <a href="#" class="navbar-brand">Navbar</a>
      <div class="collapse navbar-collapse" id="navbarResponsiveLeft">
        <ul class="navbar-nav">
          <li class="nav-item">
            <a href="#" class="nav-link active" aria-current="page">Active</a>
          </li>
          <li class="nav-item">
            <a href="#" class="nav-link">Link</a>
          </li>
          <li class="nav-item">
            <a href="#" class="nav-link disabled" tabindex="-1" aria-disabled="true">Disabled</a>
          </li>
        </ul>
      </div>
    </div>
</nav>
```

#### Small devices

![](./img/nav/other_devices.JPG)

### biggest than small devices


![](./img/nav/small.JPG)


