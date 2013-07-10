jquery.globalnav
================

This repo shows an example setup to make HTML prototypes with page states and a global menu to navigate between pages.

We are using **jQuery**, **SCSS** (optional) and **Jekyll**. You should be familiar with Jekyll to use this.

Demo
----

See [http://wolfslittlestore.be/jquery.jekyll.globalnav](demo).

How to use
----------

Run these commands and look at the generated site:

    jekyll serve -w
    compass watch

Hit ctrl+M to trigger the global navigation.

Arboretum
---------

    .                                        
    ├── README.md                            The file you are reading.
    ├── _includes                            
    │   ├── globalnav.html                   The globalnav include which is the listing of your pages
    │   ├── index-content.html               Example of working with state (see Working with state)
    │   └── pagestates                       
    │       └── example.html                 Example page state
    ├── _layouts                             
    │   └── default.html                     
    ├── config.rb                            Config file for SCSS
    ├── css
    │   └── screen.css
    ├── index-state2.html                    Example of state (see YAML front matter and index-content include)
    ├── index.html
    ├── js
    │   ├── jquery.cookie.js                 Cookies are used to save the visibility of the menu
    │   ├── jquery.globalnav.js              Javascript that manages the toggling of the menu and cookies
    │   ├── jquery.js                        jQuery
    │   └── jwerty.js                        jwerty for the shortcuts
    ├── page-2.html                          Example pages
    ├── page-3.html                          Example pages
    └── scss
        ├── _globalnav.scss                  CSS for the menu
        └── screen.scss                      Your CSS. A .hide class (tied to display: none;) is required.

Working with state
------------------

In an HTML prototype, a single page often has 2 states. For example, a form might have an error and a regular state. You can use the page states mechanism to do this. You would do it as follows:

1. Make a new file in `_includes/pagestates/` copying the contents of `_includes/pagestates/example.html`
2. In this file, add the states of your pages.
3. Add the full page content as a new include in `_includes`
4. Manage state with YAML front matter in the files in the root ./ by adding a YAML entry for example: `state: state2`

Possible improvements
---------------------

PR if you want to make an improvement!

* Don't include jwerty and use a keycode instead