# Browsers 

This is basic knowledge about how browsers work. 
A browser is an application that locates, retrieves and displays content on the WWW. 
It has a client/server model. The client is where the browser runs. 
The browser requests the information to the server, which sends back the information needed. Then, the browser
displays this content. 

## Components 

There are several layers or components in a browser

### User Interface

These are the components which the user can interact with.  
Examples of these are: 
* Button
* Bookmarks 
* Address bar
* The window itself

### Browser Engine

The job of a browser engine is to transform HTML and other resources of a web page into an interactive visual representation on a users device. 

### Rendering Engine

Software that draws text and images on the screen. The engine draws structured text from a document (like HTML) and formats it properly
based on the given style declarations (often CSS). Examples: Blink (Google Chrome). 

#### Networking

Performs implements of HTTP request and response.

#### JavaScript Interpreter

JavaScript and all other types of scripting is parsed and executed by the inbuilt interpreter.

#### UI Backend

 It can be used for painting basic images like windows or combo box. The backend exposes only a generic platform independent interface. Beneath it, user interface methods are used by the operating system.

### Data Persistence

All types of data, like cookies are saved locally by the browser. Storage mechanisms like WebSQL, FileSystem, localStorage are also supported by the browser.


## Rendering engine flow

### Parsing

Translates a document into a structure that code can use. 
It must obey the vocabulary and syntax rules. 
* Vocabulary: Which words, symbols, etc can be used
* Syntax rules: If you use a + sign, you need numbers before and after the symbol, for example. 

Examples of parsers could be: 
* Flex
* Lex
* Yacc
* Bison
I have used Bison before, for my Compilers and interpreters class, in which for our final project, we had to create our very own programming language, and have it execute. It was... hard, or at least, it took quite a while. 

Two types of parser: Conventional, and unconventional
* Conventional: Parses CSS and Javascript
* Unconventional: HTML


#### Unconventional

Why is it unconventional? Because HTML is not context free grammar. This means, as you parse the HTML, the parser is going to try to correct errors on the fly. kind of.

### Render tree

It is generated as the DOM tree is constructed. This is is made of visual elements in the order in which they are going to be displayed  
Elements in the render tree are called renderer or render objects

### Layout

Calculates position and size of the displayed elements. 
It is a recursive process, which starts at the root, the HTML tag. 
#### Global layout
Affects all renders, and handles screen resize. 

### Paint

In this step, it paints the rendered objects. 

## Sources

* https://en.wikipedia.org/wiki/Browser_engine
* https://developer.mozilla.org/en-US/docs/Glossary/Rendering_engine
* https://dev.to/arnabroychowdhury/what-are-the-major-components-of-a-modern-web-browser-3ih1
 * Kruno: How Browsers work | JSUnconf 2017