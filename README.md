## Changes

I've removed the overlay from the original library, which I found got in the way and was a bit obtrusive. In addition, I allowed for multiple images on the same page to resize independently. They will automatically center within their container and resize when they fill the container.

## Basic usage

Include the javascript and css files.

```html
<script src="js/jquery-2.1.0.min.js" type="text/javascript"></script>
<script src="js/jquery.event.move.js" type="text/javascript"></script>
<script src="js/jquery.twentytwenty.js" type="text/javascript"></script>
<link rel="stylesheet" href="css/twentytwenty.css" type="text/css" media="screen" />
```
You might need to change the paths to match your setup.


After including the files you are ready to create a container that holds two images:

```html
<div id="container1">
 <!-- The before image is first -->
 <img src="http://placehold.it/400x200&text=1" />
 <!-- The after image is last -->
 <img src="http://placehold.it/400x200&text=2" />
</div>
```

Now initialize the plugin on the window load:

```
$(window).load(function(){
  $("#container1").twentytwenty();
});
```

### Options


```js
$(window).load(function(){
  $(".twentytwenty-container").twentytwenty({
    default_offset_pct: 0.7, // How much of the before image is visible when the page loads
    orientation: 'vertical' // Orientation of the before and after images ('horizontal' or 'vertical')
  });
});
```

### Multiple instances

If you want to use multiple instances of this plugin on a single page you can target the container class:

```js
$(window).load(function(){
  $(".twentytwenty-container").twentytwenty();
});
```

## Support

- IE8+
- Firefox (latest)
- Chrome
- Safari
- Android
- iOS (iPhone, iPad)

## Dependencies

  * [jquery](http://jquery.com/)
  * [jquery.event.move](https://github.com/stephband/jquery.event.move)

## MIT Open Source License

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
