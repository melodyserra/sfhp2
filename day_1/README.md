# Introduction to HTML & CSS Workshop 
--

## Links:

[Examples](https://repl.it/@melodyserra/Examples)

[HTML Form](https://repl.it/@melodyserra/HTML-Form)

[Floats and Flexbox](https://repl.it/@melodyserra/Floats-and-Flexbox)


## What is the box model?
- One can say that every element on the page is wrapped by a box. 
- That box takes up a specific amount of space by default.
- It consists of: margins, borders, padding, and the actual content. 
	- **Content** - The content of the box, where text and images appear
	- **Padding** - Clears an area around the content
	- **Border** - A border that goes around the padding and content
	- **Margin** - Clears an area outside the border

![Stackers!](../img/stackers.png)

### What is HTML? 
- Stands for: Hyper Text Markup Language.
- It is the content of the page. 
	- e.g. header or paragraph
- Has its own default styles. 

### What is CSS?
- Stands for: Cascading Style Sheet. 
- It is the stylistic component of the page. 
- Overrides the default styles of HTML. 
	- e.g. change the color or the font-family of your header

### What is JavaScript?
- Helps increase interactivity of the page. 
- Helps with page interactions such as animations. 
- Helps with dynamic loading of content. 

## Let's Dive Deeper
### HTML:
#### Tags < >
- Allow you to set up structure of the page. 
- Tell the browser how to format content. 

`<h1>Hello World!</h1>`

#### Basic layout for an HTML file

```html
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>My First Webpage</title>
</head>
<body>
	<h1>Hello World!</h1>
</body>
</html>

```
### CSS:
- In order to run external CSS you need to link it to the HTML. This usually goes in the head tag:

`<link rel=“stylesheet” href=“css/style.css” />`

#### Basic layout for a CSS file

```css
h1 {
	color: #FF9966;
	text-align: center;
}

```
### What about different ways to organize content?

#### divs:
- Define a division.
- They are equivalent to empty rectangles. 
- They are used to format block elements that can be styled via CSS. 

`<div> </div>`

#### spans:
- They are inline elements that are normally displayed without line breaks. 

`<span> </span> `

#### input:
- Inputs allow users to enter data to be saved to a database.
- They come in different forms to facilitate the specific data entry type.

```html
<input type="text" class="form-control" />
```

#### select list:
- Select lists allow users to select options from a dropdown menu.

```html
<select>
	<option value="USA">United States</option>
</select>
```

#### button:
- Buttons are HTML elements that give users the ability to submit the data entered as well as transition to new pages.

```html
<button>My Button</button>
```
### Id's versus classes
#### Id's: 
- Are selectors. 
- They are used if you want a single, unique element. 
- By convention, they are used only once. 

HTML:

```html
<div id=“header”>
	<h1>Welcome to my website</h1>	
</div>
``` 
CSS: hash/pound sign designate an id

```css
#header{
	text-align: center;
	color: red;
}
```


#### Classes:
- Are selectors. 
- Select an element with a specific class attribute.
- Can be used more than once.  

HTML:

```html
<div class=“paragraph”>
     Here are my favorite hobbies:
     skateboarding, scuba diving, and
     riding motorcycles.
</div> 

```
CSS: a period designates a class

```css
.paragraph {
	color: green;
}

```

## Selector Exercise
- Let's use Codepen.io to practice CSS selectors.
- Create at least one div with an id, and four divs with a class.
- Use CSS to apply styling to the divs based on the id and class selectors.
- Bonus: Try implementing one or more styles using a CSS3 selector (first-child, nth-child, first-of-type, etc).

### HTML Markup Lab
- Open the `html_form` folder and open `index.html`.
- For each comment denoted by `<!-- -->` replace the comment text with the correct HTML as per the instruction to create the form.
- Bonus 1: Alter the CSS file to use a web safe font.
- Bonus 2: Use CSS to change the background color of the page. Experiment with using images as backgrounds as well.
- Double Bonus: Review the CSS `transition` property documentation and try to create a small animation anywhere on the form. An example may be to highlight a border around a form field when it is clicked.


### Margin, Padding, and the Box Model
- **Margin** clears area outside border, it is transparent. 
- **Padding** clears area around the content, it is transparent. 
- The **CSS box model** is a box that wraps around HTML elements. It consists of: the content, padding, border, and margin. This model allows us to define space around and between elements. 


![image](http://www.w3schools.com/css/box-model.gif)

## CSS Positioning
- There are four main types of positioning that you will see most often - static, relative, absolute, and fixed.
- Static positioning is what all elements have by default.
- Relative and absolute work together - elements can be positioned absolutely relative to their container.
- Fixed position elements are essentially absolute relative to the window no matter where they are in the DOM. A.K.A. the window is always the relative parent.

## Positioning Exercise
- Try to replicate the following mockups using what we've talked about in this class so far.
- Utilize margins, padding, floats, positioning, etc.

1. Stackers!

![Stackers!](../img/stackers.png)

2. The Mirror (Bonus 1)

![The Mirror](../img/the_mirror.png)

3. The Skinny (Bonus 2)

![The Skinny](../img/the_skinny.png)

4. The Absolute (Bonus 3)

![The Absolute](../img/the_absolute.png)

## Element Alignment
- To determine how we can align an element we have to first know what kind of element it is.
- Inline elements can be aligned as text, so with the `text-align` CSS property.
- Block elements can be aligned using the space around them - margin. A margin set to auto for both left and right will center the element in a container.

## Floats
- Floating elements allows us to create a nearly unlimited number of layouts using all types of block elements.
- [Floating](https://developer.mozilla.org/en-US/docs/Web/CSS/float) an element essentially removes it from the standard "flow" and places it to the left or right side of its container.
- Elements can have fixed width, which will wrap underneath each other if the container is smaller than the combined widths.
- You can also used percentage width, which will have the columns respond to the screen size.
- You can tell already that the calculations can get out of hand really fast...
- [Clear-fix](http://learnlayout.com/clearfix.html) forces content after the floats or the container containing the floats to render below it. 

## Flexbox vs. Floats

![Flexbox](../img/container.png)

- The container is called the ***flex container***
- The elements inside the container are called the ***flex items***

HTML

```html
<div>
	<section>Hello</section>
	<section>Hello 2</section>
	<section>Hello 3</section>
</div>

```

CSS 

```css
div {
	display: flex;
	justify-content: space-between;
}

```

## How can you see/edit within browser an existing webpage?
- Open the developer tools. 
- This can then be used as a “console” to test new code/change code and see what it looks like. 
