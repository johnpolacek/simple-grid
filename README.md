#Simple Grid

A simple, easy-to-use 12-column responsive grid with some nice features. Built with [Simple Grid Generator](https://github.com/johnpolacek/simple-grid-generator).

For an example implementation, check out the [Expressive CSS Project Page](http://johnpolacek.github.io/expressive-css/).

##Features

###Responsive Overrides
Set the default grid width, then override at different screen widths with breakpoint prefixes.

```
<div class="grid-3 m-grid-6 s-grid-12">
<!-- 
	Translates to: 
		- Quarter width by default
		- Half width at the medium breakpoint
		- Full width at the small breakpoint
-->
```

###Padding & Margin Classes
For quick, easy layouts, use the grid to set consistent padding and margin on all your elements (top, bottom, left, right, horizontal, vertical, all). 

By default, there are 4 levels of padding/margin you can apply (or none).

```
/* For example... */
.pad-0 { padding: 0; }
.pad-1 { padding: 0.25em; }
.pad-2-sides { padding-left: 0.5em; padding-right: 0.5em; }
.pad-4-bottom { padding-bottom: 2em; }
.marg-3-vertical { margin-top: 1em; margin-bottom: 1em; }
```
Breakpoint prefixes can also be used to easily make layout adjustments for different screen widths.

```
<div class="pad-2 m-pad-1 s-pad-0">
```

###Equal Height Grid Containers
For responsive grid columns that have matching heights regardless of their inner content, use `.grid-flex`.

```
.grid-flex {
    display: flex;
    flex-wrap: wrap;
}
```
Use this class on the parent grid container.

```
<div class="grid-12 grid-flex">
	<div class="grid-12 m-grid-6 l-grid-3"></div>
	<div class="grid-12 m-grid-6 l-grid-3"></div>
	<div class="grid-12 m-grid-6 l-grid-3"></div>
	<div class="grid-12 m-grid-6 l-grid-3"></div>
</div>
```

*Note: this solution relies on Flexbox layout mode. Refer to [caniuse.com](http://caniuse.com/#feat=flexbox) for broswer support information. Browser prefixes removed for brevity.*


##Setting Up

Do any of the following:

- Simply put the contents of grid.min.css into your stylesheet
- If you have a CSS build process with minification and concatenation, include grid.css in your configuration.
- If using SASS, include the contents of the `/sass` directory in your project. Read below fo customization options.


##Customize With Sass
If you are familiar with Sass, you can use the [Simple Grid Generator](https://github.com/johnpolacek/simple-grid-generator) mixin to set your own values for:

###Number of Columns
Switch to a 18-column or 24-column grid instead.

###Breakpoints and Breakpoint Prefixes
Change the breakpoints, or add in more. Name the prefixes whatever you like xs-, xl-, etc.

###Padding and Margin Classes
Add more, take some away. Set the values however you like, px or em. Use only padding (no margin) or just remove them altogether.

**For more information, go to the [Simple Grid Generator Project Page](https://github.com/johnpolacek/simple-grid-generator).**

##License
Author & copyright (c) 2015: [John Polacek](http://johnpolacek.com), Dual MIT & GPL license