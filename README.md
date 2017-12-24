# Start Page Tutorial

## 1 Tooling up

### 1.1 Text Editors

To start with you're going to need a text editor. You can techinically use anything on your PC that will allow you save text, such as Notepad however I recommend that you install a proper one.

___Note:__ Before you get ahead of yourself thinking that it would be worth using Notepad just because it's shit. Don't. Nobody cares. All it signals is that you're a hipster or you like unnecessary pain._

Text editors that I have used and do recommend are:
* Sublime Text 3 (Sublime)
* Atom
* Visual Studio Code (VS Code)

A couple of other popular ones are:
* Notepad++
* Brackets

_Note:_ One nice feature of Brackets is that it has a 'live preview' feature, meaning that it will auto-refresh your browser when you save the file. Last time I tried using it however, the live preview kept breaking. Your mileage may vary.

The reason I recommend that you install a proper text editor such as one of these is for two main reasons:
1. They allow you to install extensions. These extensions have a wide range of uses such as:
	* Checking for errors in your code
	* Allowing you to convert colours between formats such as hexadecimal (#ffffff) to rgb (255, 255, 255)
	* Auto-completing code
2. They use syntax highlighting to highlight different types of code. For example, a HTML element can be structured like this:
    ```
    <p class="text-centre">Centred text</p>
    ``` 
    Syntax highlighting makes it easier to read the code by highlighting different parts in different colours. Meaning that in your editor that code could look like this: 
    ```html
    <p class="text-centre">Centred text</p>
    ```
    This makes your code easier to read because, once you understand the components of it, you will be able to tell quickly, and at a glance, what you're looking at without having to read other code for context. Syntax highlighting can also help to catch errors. For example, trying to select an ID with CSS typically uses a different colour to a class selector. So it's easier to tell at a glance that ```#about``` is not the same as ```.about```.


### 1.2 Plugins

The only plugin I'd really recommend that you use from the start is Emmet. Emmet adds shortcuts for writing code. Don't worry about not learning properly. You still need to understand what you're writing. Emmet just takes the tedium out of it. For example, a HTML tag looks like this:
```html
<div></div>
```

Rather than typing that out. You can simply type: `div`, then press `tab`, and Emmet will convert that to the above code.

There are other shortcuts too, such as the following: `.container>.row*2>a.link-unstyled`. Which will become the following:
```html
<div class="container">
    <div class="row">
        <a href="" class="link-unstyled"></a>
    </div>
    <div class="row">
        <a href="" class="link-unstyled"></a>
    </div>
</div>
```
___Note:__ Don't worry about learning complicated shortcuts for now. Instead, just remember that typing the name of the element you want, then pressing tab, will create that element for you._

#### 1.2.1 Installing Plugins

I'm going to show you how to install Emmet on the three text editors I've recommended. If you're using another one, you're on your own.

##### Sublime Text 3

Sublime is the most difficult of the three editors to install a plugin on.
1. First of all visit the [Package Control Installation page](https://packagecontrol.io/installation) and follow the instructions on there.
2. In Sublime hit `Ctrl+Shift+P`, then begin to type _"install"_ and _"Package Control: Install Package"_ should be an available option. Use your arrow keys if necessary to highlight the option, then press `Enter`. After a few seconds a similar window should appear, search for _"Emmet"_. Use your arrows keys again if necessary to highlight the package, then press `Enter` to install it.

##### Atom

1. Either hit `Ctrl+Comma` or go to `File > Settings`.
2. In the _"Install"_ tab accessed via the sidebar, search _"Emmet"_ and click _"Install"_.

##### Visual Studio Code

1. Do nothing. Emmet is pre-installed.

## 2 Setting up the project

### 2.1 Project folder

First of all you're going to create a project folder which will be opened within your text editor. This allows you to manage your files easily, with a good folder structure.
1. In your chosen code editor, go to `File > Open Folder...`.
2. From here create a folder to contain your project files and then select that folder to open it within your editor.
3. You should be able to see your folder within your side panel.

___Note:__ At times during this tutorial I may refer to the project folder as the "root directory"._

### 2.2 Folder structure and project files

Now within the project folder you are going to create two folders: `css` and `js`. These are for your CSS and JavaScript files respectively.

You can either create these folders from the File Explorer, or from your text editor. I'd recommend doing so from your text editor so that you can get used to managing a project from within.
1. In the side panel in which your project folder appears in your text editor, right click an empty space beneath your project folder and select _"New Folder"_, then name it _"css"_.
2. Repeat step 1, this time creating a folder called _"js"_.

Next you need to create a HTML file, a CSS file and a JavaScript file. To do so in your text editor once again right click the project files panel, but select _"New File"_ this time.
* In your _root directory_ create a file called _"index.html"_.
* In the _"css"_ folder create a file called _"main.css"_.
* In the _"js"_ folder create a file called _"scripts.js"_.

___Note:__ It is a good idea to create a folder structure such as this to create an easily navigatable project structure. Whilst not completely necessary for this project it is good practice for larger projects which require deeper folder structures._

## 3 Starting with the basics

### 3.1 Writing your first lines of HTML

In the index.html file you created type `html:5` and then press `tab`. If you've installed Emmet correctly in your editor "html:5" should have been converted into a template for your HTML page. If it didn't work, verify that Emmet is installed, and look at the bottom-right of your text editor. There it should say _"HTML"_ somewhere in that corner. If instead you see _"Plain Text"_ or the name of another language, click it and change the current document type to HTML. Doing so will ensure that your text editor recognises the current file as HTML and treats it accordingly.

The HTML5 template that Emmet creates varies slightly depending on text editor, but at the very least you should be able to see the following:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <title>Document</title>
</head>
<body>
    
</body>
</html>
```

This is the bare minimum that you ought to have for your HTML page.

The `<!DOCTYPE html>` tag is an instruction to the browser to tell it that the file it is reading is a HTML5 file, HTML5 being the latest version of HTML.

The following code is broken down as follows:

1. Everything in your file should be contained within the `<html></html>` tags. Your browser will recognise the contents of this as HTML and will attempt to make use of it.
    * It's worth noting that, as with most HTML tags, the HTML tag has to be opened and closed. Just like brackets. The _"html"_ within it tells the browser what this element is, and the browser will then determine how to make use of that element. An opening tag only requires angled brackets and the name of the element. A closing tag is similar, however a forward slash (_"/"_) is used to tell the browser to close the element.
    * The opening tag also has an attribute, which is __"lang="en""__. Attributes can be used for many different things and we will be making use of some in this tutorial. In this case however; the _"lang"_ attribute is telling the browser that all of the content within the `html` tag is in English.
2. Within the `<html>` element there are two main tags: `<head></head>` and `<body></body>`. These have completely separate functionality from one another.
    1. The `<head>` tag contains meta-information for your page. The current `<title></title>` tag that exists inside of the `<head>` doesn't actually appear on your web page. Instead it appears as the pages title in your browser tab.
    The `<head>` tag is also used to import extra files for your web page. For example, the `.css` and `.js` files you created earlier will be imported via the `<head>`.
    2. Inside the `<body>` resides all of the content you want to see on your web page. The browser will display the contents of this tag to you.

### 3.2 Obligatory 'Hello World!'

The first step to writing your HTML is to create a _"Hello World!"_.

Start by adding a paragraph inside your `body` tag. In order to do this either type `p` and then press `tab` for Emmet to autocomplete your element, or type `<p></p>`. Between these `<p>` tags, add _"Hello World!"_. Your body tag should look like this:

```html
<body>
    <p>Hello World!</p>
</body>
```

Now save that and open the file in your browser to see your heading.

Your message probably doesn't look very grand. The reason being that the `<p>` tag is the default element used for paragraphs, which typically aren't very large. So your browser will style that as if it were normal text. We want our message to be big though, otherwise will anybody read it?

Change the paragraph tag to a heading tag. For this example we'll use `<h1>` or _"heading 1"_. There are six types of heading _h1_ to _h6_. Each of these is supposed to represent a hierarchy of importance. A `h1` is the most important and as such should only be used once on your page. All other heading tags can be used as many times as you'd like.

Your body tag should now look like this:

```html
<body>
    <h1>Hello World!</h1>
</body>
```

Refreshing your browser should now reveal that your message is bold and much bigger than your paragraph was.

### 3.3 Moving on to the lists

Now that you have an understanding of how to make some HTML elements, we'll start making this start page. The start page is going to have two main components: lists and links.

We'll start with the lists first because the links are contained within them. To start creating your first list there are two different types of list to know about: ordered and unordered. The difference between the two is simply that an ordered list is labelled: "1, 2, 3...", whereas an unordered list is a bulleted list.

Since the list you're making presumably has no ranking importance for the list items, we'll use an unordered list.

In order to create one make a `<ul>` tag, and don't forget to close it! _Note: `ul` means "unordered list" and `ol` means "ordered list"._

From here if you add content inside of your `ul` tag such as your "Hello World!" message, you won't find any bullet points. This is because the browser does not yet recognise that content as a list item. In order to make a list item we use the `<li>` tag. If you're being rebellious and you're using an ordered list instead, the `li` tag is still the tag that you want to use for list items (and don't worry about numbering them; the browser will do that for you). Within the list item, we add our content. So, for example, if I was listing web development related sites my list might look something like this:

```html
<ul>
    <li>Mozilla Development Network</li>
    <li>W3Schools</li>
</ul>
```

Currently, the list shown above isn't very useful because it just names the websites. Let's convert these items into links that we can use to quickly access those sites.

To do this we need to use the `<a></a>` tag, also known as the _"anchor"_ tag. Similarly to the other elements we've created so far, we add the text that we want to see on the page between those opening and closing tags, such as `<a>Mozilla Development Network</a>`. You are probably wondering right now how the browser knows where to send the user. This is where the `href` attribute comes in. If you create your `a` tag using Emmet, it will automatically add the `href` attribute to your opening tag. Otherwise make your opening tag look like this `<a href=""></a>`. Between those quote marks you paste the URL of the page you want to link to.

Your HTML should end up looking something like this:

```html
<ul>
    <li>
        <a href="https://css-tricks.com/">CSS Tricks</a>
    </li>
    <li>
        <a href="https://developer.mozilla.org/en-US/">Mozilla Development Network</a>
    </li>
    <li>
        <a href="https://www.w3schools.com/">W3Schools</a>
    </li>
</ul>
```
Note that if you try adding the _"href"_ attribute to another element, such as one of your `li` tags, it won't turn that element into a clickable link. That's because the browser doesn't give that ability to other elements.

### 3.4 Task

For now, try using what you've learnt so far to create multiple lists. Organise some of your bookmarks into categories, add a heading to each list and then create list items for each bookmark within those categories.