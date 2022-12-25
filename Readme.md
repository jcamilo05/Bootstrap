# This repo contains some useful information about Boostrap 5 

## BREAKPOINTS

In bootsrap there are **6 default breakpoints**  

**Extra small: < 576px**  
**Small: >= 576px (sm)**  
**Medium: >= 768px (md)**
**Large: >= 992px (lg)**  
**Extra Large: >= 1200px (xl)**  

## Grid System

Bootstrap's grid system uses a series of containers, rows and columns to layout and align content.

### Columns

Boostrap support until 12 columns, the column's number desired must be specified, otherwise this will be automatically adjust to the screen size.

**Equal widht**  

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

The previus code, look like the following image.


![](./img/notes/equalCol.JPG)


**One column width**

A column can be set with a predifined width, one can predifined how many columns set in a row, but taking in account that the max of columns is 12, so for example the following chunk of code set the second column with 7, and the otrhers two columns are adjust automatically, all depend of screen size.

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
The columns can be set to resize depending on the size screen, so for example the following code set 3 differents possible values, the first one when the device is small, and can put until 12 columns, the second one is setted for medium device what is setted until 6 columns, and the last one which is setted to large devices.

```html
<div class="row">
    <div class="col-12 col-md-6 col-lg-3 border">.col-12 .col-md-6 .col-lg-3</div>
    <div class="col-12 col-md-6 col-lg-3 border">.col-12 .col-md-6 .col-lg-3</div>
    <div class="col-12 col-md-6 col-lg-3 border">.col-12 .col-md-6 .col-lg-3</div>
    <div class="col-12 col-md-6 col-lg-3 border">.col-12 .col-md-6 .col-lg-3</div>
</div>

```
The previous settup put one column until 768px that is when a medium size begins, then it will have 2 columns until get 992px that is when the larger size is taken.

The following screenshots shows the previous paragraph.

#### small size (until 768px)


![](./img/notes/smallResp.JPG)

#### Medium size (until 992px)

![](./img/notes/mediumResp.JPG)

#### Large size (until 992px)

![](./img/notes/largeResp.JPG)

###CSS note

```css
div[class^="test"]{
    background: #fff;
```
The meaning of the previous notation is set a background to all divs which have a class name of test

## Vertical aligments

The columns can be align horizontally with the following 3 tags.

```html
<div class="row align-items-start"></div>
<div class="row align-items-center"></div>
<div class="row align-items-end"></div>
```

the previous 3 aligments look like the following images

![](./img/notes/verticalAlig.JPG)

## Horizontal aligment

There are 6 different to set the horizontal aligment with Bootstrap

The following chunk, shows the 6 tags available to set the horizaontal aligments and how it looks like..

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


