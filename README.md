I HATE COOKING FOOD, SO I WILL DO 3 RACING DRIVERS WITH SOME STATS AND INFO ABOUT.

Will have the same structure, just different content.



Here ill put my notes for HTML and CSS:




###### HTML ######

**** Basic structure of a HTML document: ****

////////////////////////////////////////////////////////////////////////////////////////

<!DOCTYPE html>

<html lang="en">

<head>
  <meta charset="utf-8">
  <title>First Webpage</title>

</head>

<body>
  <!-- ////////////////////
    ////// HEADINGS /////////
    ///////////////////// -->

  <!-- Headings are different from other HTML text elements: they are displayed larger and bolder than other text to signify that they are headings.

There are 6 different levels of headings starting from <h1> to <h6>. The number within a heading tag represents that heading’s level. The largest and most important heading is h1, while h6 is the tiniest heading at the lowest level. -->

  ##
  <h1>Hello Motherfuckers!</h1>


  <!-- ////////////////////
    ////// PARAGRAPHS ///////
    ///////////////////// -->

  <!-- to separate paragraphs <p> </p> -->

  ## <p>
    paragraph 1
  </p>
  <p>
    paragraph 2
  </p>

  <!-- ////////////////////
    ///// <main></main> ///
    /////////////////// -->

  ## HTML5 has some elements that identify different content areas. These elements make your HTML easier to read and
  help with Search Engine Optimization (SEO) and accessibility.

  Example:

  <main>
    <h1>CatPhotoApp</h1>
    <h2>Cat Photos</h2>
    <!-- TODO: Add link to cat photos -->
    <p>See more cat photos in our gallery.</p>
  </main>


  <!-- ////////////////////
    ///////// LISTS /////////
    ///////////////////// -->

  <!-- Unordered lists are created using the <ul> element, and each item within the list is created using the list item element <li>. 
        Each list item in an unordered list begins with a bullet point:-->

  ##
  <ul>
    <li>1</li>
    <li>2</li>
    <li>3</li>
  </ul>

  <!-- Ordered lists are created using the <ol> element. Each individual item in them is again created using the list item element <li>. However, each list item in an ordered list begins with a number instead: -->

  ##
  <ol>
    <li>1</li>
    <li>2</li>
    <li>3</li>
  </ol>


  <!-- /////////////////////
    ////////// LINKS /////////
    /////////////////////  -->

  <!-- OPENING LINKS IN ANOTHER TAB -->
  <!-- "anchor <a></a>": any text wrapped with an anchor<a></a> tag without a href attribute will look like plain text. If the "href" attribute is present, the browser will give the text a blue color and underline it to signify it is a link. example: <a href="link"> string </a> -->

  <!-- "target": attribute is used to specify where the linked document will open when the link is clicked. The target attribute can have one of the following values: "_blank" - Opens the linked document in a new window or tab, "_self" - Opens the linked document in the same window/tab as it was clicked (this is default), "_parent" - Opens the linked document in the parent frame, "_top" - Opens the linked document in the full body of the window, "_framename" - Opens the linked document in a named frame  -->

  <!-- "rel": it is recommended to always pair a target="_blank" with a rel="noopener noreferrer". "rel" is used for security reasons. It stands for "relationship" and is used to describe the relationship between the current document and the linked document. "noopener" prevents the new page from being able to access the window.opener property and ensures it runs in a separate process. "noreferrer" has the same effect, but also prevents the Referer header from being sent to the new page. This header contains information about the current page that the new page could use to track where the request came from. -->

  ##
  <a href="https://www.theodinproject.com/about/" target="_blank" rel="noopener noreferrer">Click here</a>

  <!-- Absolute and relative links -->

  <!-- Links to pages on other websites on the internet are called absolute links. Like the one we used above this -->
  <!-- example: <a href="https://www.theodinproject.com/about/" target="_blank" rel="noopener noreferrer">Click here</a> -->

  <!-- Links to other pages on the same website are called relative links. -->
  <a href="./pages/about.html">About</a>


  <!-- /////////////////////
    ///////// IMAGES /////////
    ////////////////////// -->

  <!-- Images are inserted using the <img> element. The <img> element is an empty element, meaning it does not need a closing tag. -->

  <!-- If we want to load the .jpg in the about sub link we need to use the relative path. example: <img
        src="../images/charlesdeluvio-Mv9hjnEUHR4-unsplash.jpg"> in the about.html code file -->

  The src="url" attribute in an img element specifies the image's URL (where the image is located).

  <!-- Image size attributes: 'height' and 'width'
    While not strictly required, specifying height and width attributes in image tags helps the browser layout the page without causing the page to jump and flash.
    example: <img src="image.jpg" alt="image" height="100" width="100"> -->

  <!-- All img elements should have an alt attribute. The alt attribute's text is used for screen readers to improve accessibility and is displayed if the image fails to load. For example, <img src="cat.jpg" alt="A cat"> has an alt attribute with the text A cat. -->

  <img src="./images/charlesdeluvio-Mv9hjnEUHR4-unsplash.jpg" alt="The Doggo" height="853" width="640">

  ##

  <script src="scripts/testingscripts.js"></script>

</body>

</html>

////////////////////////////////////////////////////////////////////////////////////////

**** This is the code for the about.html page that is linked in the index.html ****

<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <title>Odin Links and Images</title>
</head>

<body>
  <h1>About Page</h1>
  <!-- If we want to load the .jpg in the about sub link we need to use the relative path. example: <img
        src="../images/charlesdeluvio-Mv9hjnEUHR4-unsplash.jpg"> in the about.html code file -->
  <img src="../images/charlesdeluvio-Mv9hjnEUHR4-unsplash.jpg" alt="The Doggo" height="853" width="640">

</body>

</html>




###### CSS ######

SELECTORS
## Universal Selector:
* {
color: purple;
}

The universal selector will select elements of any type, hence the name “universal”, and the syntax for it is a simple
asterisk. Every element would have the color: purple; style applied to it.


## Type Selector:

<!-- index.html -->

<div>Hello, World!</div>
<div>Hello again!</div>
<p>Hi...</p>
<div>Okay, bye.</div>

<!-- style.css -->
div {
color: white;
}

Here, all three <div> elements would be selected, while the <p> element wouldn’t be.


    ## Class Selector:

    <!-- index.html -->

  <div class="alert-text">Please agree to our terms of service.</div>

  /* styles.css */

  .alert-text {
  color: red;
  }

  Note the syntax for class selectors: a period immediately followed by the case-sensitive value of the class attribute.
  Classes aren’t required to be specific to a particular element, so you can use the same class on as many elements as
  you want.

  Another thing you can do with the class attribute is to add multiple classes to a single element as a space-separated
  list, such as:
  class="alert-text severe-alert"
  Since whitespace is used to separate class names like this, you should never use spaces for multi-worded names and
  should use a hyphen instead.


  ## ID Selector:

  <!-- index.html -->

  <div id="title">My Awesome 90's Page</div>

  /* styles.css */

  #title {
  background-color: red;
  }

  ID Selectors are similar to class selectors, but they’re more specific. They’re also used less often, since they can
  only be used once per page. The syntax for ID selectors is a hash symbol immediately followed by the case-sensitive
  value of the id attribute.
  While there are cases where using an ID makes sense or is needed, such as taking advantage of specificity or having
  links redirect to a section on the current page, you should use IDs sparingly (if at all).

  ## The grouping selector

  .read {
  color: white;
  background-color: black;
  /* several unique declarations */
  }

  .unread {
  color: white;
  background-color: black;
  /* several unique declarations */
  }

  The grouping selector allows you to apply the same styles to multiple selectors. In the example above, the .read and
  .unread classes have the same styles, so we can group them together like this:

  .read,
  .unread {
  color: white;
  background-color: black;
  }

  .read {
  /* several unique declarations */
  }

  .unread {
  /* several unique declarations */
  }

  ## Chaining Selectors:

  <!-- index.html -->
  <div>
    <div class="subsection header">Latest Posts</div>
    <p class="subsection preview">This is where a preview for a post might go.</p>
  </div>


  We have two elements with the subsection class that have some sort of unique styles, but what if we only want to apply
  a separate rule to the element that also has header as a second class?

  <!-- styles.css -->
  .subsection.header {
  color: red;
  }

  What
  .subsection.header
  does is it selects any element that has both the subsection and header classes. Notice how there isn’t any space
  between the .subsection and .header class selectors.
  The style rule will only be applied when the both classes are present on the same element. If the element only has one
  of the classes, the style rule won’t be applied.
  This can also be applied to IDs, so if you had an element with the id of title and the class of header, you could
  select it like this:

  <!-- HTML -->
  <div>
    <div class="subsection header">Latest Posts</div>
    <p class="subsection" id="preview">
      This is where a preview for a post might go.
    </p>
  </div>

  <!-- CSS -->
  .subsection.header {
  color: red;
  }

  .subsection#preview {
  color: blue;
  }

  In general, you can’t chain more than one type selector since an element can’t be two different types at once. For
  example, chaining two type selectors like div and p would give us the selector divp, which wouldn’t work since the
  selector would try to find a literal <divp> element, which doesn’t exist. However, you can chain a type selector with
    a class or ID selector, like div.header or p#preview.

    ## Descendant combinator
    There are four different types of combinators, here we will only be covering the descendant combinator, which is the
    most common one. The descendant combinator is a space ( ) that separates two selectors. It matches elements that are
    descendants of the first selector (also called the ancestor), as long as they also match the second selector.

    <!-- index.html -->

    <div class="ancestor">
      <!-- A -->
      <div class="contents">
        <!-- B -->
        <div class="contents"><!-- C --></div>
      </div>
    </div>

    <div class="contents"></div>
    <!-- D -->

    <!-- styles.css -->

    .ancestor .contents {
    /* some declarations */
    }

    This will only apply to the elements marked A, B, and C in the HTML above. It won’t apply to the element marked D
    since it’s not a descendant of an element with the ancestor class.
    Basically it means that the element with the ancestor class will be selected, and then any element with the contents
    class that is a descendant of the element with the ancestor class will also be selected.

    //////////////////////////////////////////////////////

    ## Properties to get started with

    Color and background-color

    The color property is used to set the color of text, while the background-color property is used to set the color of
    an element’s background. The value of both properties can be any valid CSS color, such as a color name, hex code, or
    RGB value.

    <!-- CSS -->

    p {
    /* hex example: */
    color: #1100ff;
    }

    p {
    /* rgb example: */
    color: rgb(100, 0, 127);
    }

    p {
    /* hsl example: */
    color: hsl(15, 82%, 56%);
    }

    we can also use the color name, like this:

    p {
    /* color name example: */
    color: red;
    }

    how you can adjust the opacity of these colors by adding an alpha value. The alpha value is a number between 0 and
    1, where 0 is completely transparent and 1 is completely opaque. To add an alpha value, you can use the rgba() or
    hsla() functions instead of the rgb() or hsl() functions. The first three values are the same as the rgb() and hsl()
    functions, while the fourth value is the alpha value.
    https://www.w3schools.com/cssref/css_colors_legal.php

    ## Typography basics and text-align

    # Font family
    font-family
    property is used to set the font of an element. The value of the property is a comma-separated list of font names,
    with the first font being the preferred font. If the first font isn’t available, the browser will try the next font
    in the list, and so on. If none of the fonts are available, the browser will use its default font.

    If a browser cannot find or does not support the first font in a list, it will use the next one, then the next one
    and so on until it finds a supported and valid font. This is why it’s best practice to include a list of values for
    this property, starting with the font you want to be used most and ending with a generic font family as a fallback,
    e.g.

    <!-- font-family: "Times New Roman", serif; -->

    # Font size

    font-size
    Will, as the property name suggests, set the size of the font. When giving a value to this property, the value
    should not contain any whitespace, e.g. font-size: 22px has no space between “22” and “px”.

    font-weight
    Affects the boldness of text, assuming the font supports the specified weight. This value can be a keyword, e.g.
    font-weight: bold, or a number between 1 and 1000, e.g. font-weight: 700 (the equivalent of bold). Usually, the
    numeric values will be in increments of 100 up to 900, though this will depend on the font.

    text-align
    will align text horizontally within an element, and you can use the common keywords you may have come across in word
    processors as the value for this property, e.g. text-align: center.

    ## Image height and width
    By default, an <img> element’s height and width values will be the same as the actual image file’s height and width.

    Its best practice to

    <!-- CSS -->

    img {
    height: auto;
    width: 500px;
    }

    Its good to use auto for the height because it will use the same ratio if we change the width and the image will not
    be distorted.
    For example, if an image’s original size was 500px height and 1000px width, using the above CSS would result in a
    height of 250px.

    its best to include both of these properties for <img> elements, even if you don’t plan on adjusting the values from
    the image file’s original ones. When these values aren’t included, if an image takes longer to load than the rest of
    the page contents, the image won’t take up any space on the page at first, but will suddenly cause a drastic shift
    of the other page contents once it does load in. Explicitly stating a height and width prevents this from happening,
    as space will be “reserved” on the page and will just appear as a blank space until the image loads.


    ### Adding CSS to HTML

    Mostly is recommended to use an external CSS file, but you can also use the <style>
      tag in the <head>of your HTML document to add CSS to your page. This is called an internal stylesheet. < !-- index.html --><head><link rel="stylesheet" href="styles.css" /></head>
      /* styles.css */

      div {
        color: white;
        background-color: black;
      }

      p {
        color: red;
      }

      First,
      we add a self-closing <link>element inside of the opening and closing <head>tags of the HTML file. The href attribute is the location of the CSS file,
      either an absolute URL or,
      what you’ll be utilizing,
      a URL relative to the location of the HTML file. In our example above,
      we are assuming both files are located in the same directory. The rel attribute is required,
      and it specifies the relationship between the HTML file and the linked file. Then inside of the newly created styles.css file,
      we have the selector (the div and p),
      followed by a pair of opening and closing curly braces,
      which create a “declaration block”. Finally,
      we place any declarations inside of the declaration block. color: white;
      is one declaration,
      with color being the property and white being the value,
      and background-color: black;
      is another declaration. A note on file names: styles.css is just what we went with as the file name here. You can name the file whatever you want as long as the file type is .css,
      though “style” or “styles” is most commonly used. A couple of the pros to this method are: 1. It keeps our HTML and CSS separated,
      which results in the HTML file being smaller and making things look cleaner. 2. We only need to edit the CSS in one place,
      which is especially handy for websites with many pages that all share similar styles.