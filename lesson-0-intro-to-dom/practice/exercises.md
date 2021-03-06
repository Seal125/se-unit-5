# Unit 5 Lesson 0 Practice
## Intro to the DOM and Trees

1. Write a brief description of what the DOM is.
- The DOM, aka the Document Object Model, is a representation that any language can use to layout their webpage with HTML. It also makes webpages interactive, and the common way to make it interactive is by using JavaScript - in fact, most of the time, the DOM relates to using JavaScript, or ejs, in DOM's for responsive purposes.

2. Draw a diagram of the DOM tree for the `sample.html` file below.

      ```html
      <html>
          <head>
              <h1>Hello</h1>
          <head>
          <body>
              <p id="school">Marcy Lab</p>
              <p id="chief-program-officer">Maya</p>
          </body>
      </html>
      ```

#   Document
#      |
#     html
     _ | _ _ _
    |         |
  head       body
  _ |          | _
 |                |
 h1               p
 |             _  |  _
Hello         |       |
        Marcy Lab    Maya

3. Convert the tree below to HTML code.
![dom-tree](dom-tree-diagram.png).

```html
<!DOCTYPE html>
<html>
  <head>
    <title>My Title</title>
  </head>
  <body>
    <h1>My header</h1>
    <a href="/randomlink">My link</a>
  </body>
</html>
```

4. How many nodes does the following HTML snippet have. Draw the DOM tree.
      ```html
      <div>
        <p>Then press the <em>Draw</em> button</p>
      </div>
      ```

                Document
                   |
                 html
               _ _ | _ _
              |         |
            head       body
                        |
                       div
                    _ _ | _ _
                   |    |    |
                  ''    p    ''
                    _ _ | _ _
                   |    |    |
      'Then press the'  em   'button'
                         |
                       'Draw'

There are 12 nodes, because when you have the elements look nested inside another element, you're essentially adding a text node as a space.

5. How many nodes does the following HTML snippet have. Draw the DOM tree.
      ```html
      <div><p>Then press the <em>Draw</em> button.</p></div>
      ```

                            Document
                               |
                              html
                           _ _ | _ _
                          |         |
                        head        body
                                      |
                                     div
                                      |
                                      p
                                  _ _ | _ _
                                 |         |
                    'Then press the'  em   'button'
                                      |
                                    'Draw'
There are 10 nodes, since you're not nesting any elements - it's all in one line.

6. How many direct and indirect child nodes does each parent node — starting with the element with an id of 1 — have in the DOM generated by the following HTML:
      ```html
      <div id="1">
        <h1 id="2">Hello, <em id="3">World</em></h1>
        <p id="4">
          Welcome to wonderland. This is an
          <span id="5">awesome</span> place.
        </p>
        <a href="#" id="6"><strong id="7">Enter</strong></a>
        <div id="8"><p id="9"><a href="#" id="10">Go back</a></p></div>
      </div>
      ```
    Consider the following when counting the direct and indirect child nodes for each parent node:

    * Any DOM node that has at least one child node is a parent node.
    * Indirect child nodes are the child nodes of child nodes
