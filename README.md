# Start Page Tutorial
### By David Warrington

## 1 Tooling up
---

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
    This makes your code easier to read because, once you understand the components of it, you will be able to tell quickly, and at a glance, what you're looking at without having to read other code for context. Syntax highlighting can also help to catch errors. For example, trying to select an ID with CSS typically uses a different colour to a class selector. So it's easier to tell at a glance that ```#about``` is not the same ```.about```.


### 1.2 Plugins

The only plugin I'd really recommend that you use from the start is Emmet. Emmet adds shortcuts for writing code. Don't worry about not learning properly. You still need to understand what you're writing. Emmet just takes the tedium out of it. For example, a HTML tag looks like this:
```html
<div></div>
```

Rather than typing that out. You can simply type: `div`, then press tab, and Emmet will convert that to the above code.

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

