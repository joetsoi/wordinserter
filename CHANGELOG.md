## 0.9.4.4
Fix Heading element not being correctly rendered, and fix cell table widths throwing an error if they are 
pixel based but the parents are percentage based

## 0.9.4.3
Fix for some python 3.5 specific syntax

## 0.9.4.2
Ignore text elements from child validation

## 0.9.4.1
Don't error with images that have no src attribute.

## 0.9.4
Add support for rotated text in table cells

## 0.9.3
Correctly handle CSS inheritance: child styles are applied after the parent ones (before this they were
applied top down, children first). This means child styles correctly override parent ones.

## 0.9.2.7
Handle broken images correctly. If an image is invalid then the `404.png` will be inserted.

## 0.9.2.6
Handle hyperlinks after lists correctly.

## 0.9.2.5
Improve error support, InsertErrors now store the `exc_info()` of the 
inner exception.

## 0.9.2.4
Fix CodeBlock spacing styles being incorrectly reverted after the 
CodeBlock has finished.

## 0.9.2.3
Improve list formatting

## 0.9.2.2
Fix using int() when floats are expected.

## 0.9.2
Fix handling of background colors

## 0.9.1
Fix table cell range handling. 

## 0.9
Don't do the formatting "x" hack unless there is actually a format to apply. Improved the speed of table creation.
Disabled spell checking for code blocks. All nodes now support an "id" attribute, and if it is specified in a 
heading tag a bookmark is added with the ID attribute as its name. Hyperlinks also now support a bookmark if their 
URL's start with a "#", so `<a href="#name">` would link to `<h1 id="name">`.

Majorly refactored the whitespace handling code. It not actually works :)

## 0.8.8
Fix line spacing after CodeBlocks. Added support for border styles in images, and for multiple constants (use the
`CombinedConstants` class)

## 0.8.7
Added support for CSS files! WHERE IS YOUR GOD NOW? You can pass a `stylesheets` array to `parse()` with some css
definitions and it will do the right thing.

## 0.8.6
Added support for images with data URIs. Passing an image with a src set to "data:mimetype,base64;DATA..." will work
as expected, by extracting the image from the data URI and saving it, before inserting.

## 0.8.5
Remove `break_across_pages`. Word is horrible, you need to make the application Visible=True for
this to work. This should be handled by your app code not this library.

## 0.8.4
Add an attribute `break_across_pages` to the Table operation. Add this to make your tables break
across pages, hopefully.

## 0.8.3
Fix an encoding error on Windows Server. Why windows, why. :(

## 0.8.2
Fixed an error when an unknown language is given inside a code block.

## 0.8.1
Refactored the lists implementation to not suck and actually function. We now support roman numerals,
complex nested lists and other funky stuff. Added a `lxml` dependency and hard-coded the parser to be `lxml`.

## 0.8.0
Remove pywin32 dependency

## 0.7.9
Add support for table cells with background colors.

## 0.7.8
Actually handle ListElements with no children

## 0.7.7
Handle ListElements with no children

## 0.7.6
Apparently there is already a 0.7.5 release. Not sure how that happened.

## 0.7.5
Added support for CSS named colors, i.e `color: black`.

## 0.7.4
Callbacks are now called **after** the operation has been styled, instead of before.

## 0.7.3
Hopefully improved whitespace handling inside `ListElements`, and improved the logic behind `LineBreak` operations.

## 0.7.2
Fixes for table cells with no width, also always ensure a `Format` object is attached to an Operation.

## 0.7.1
Added support for tables with percentage widths.

## 0.6.13
Added support for text-align CSS classes inside tables

## 0.6.12
Added support for <br> tags.

## 0.6.11
Fixed an issue where inserting an image as the only content of a TableCell would cause it to be inserted in the wrong place.