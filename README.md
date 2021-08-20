# yes-script
The opposite of `<noscript>`.

The code contained in this repo is in the public domain.

--------

I like to write my webapps in such a manner that people don't need JS to use them. Occasionally, however, there's a feature I want to add (such as a 'copy to clipboard' button) that only works with JS.

To make the webapp neater, I only want such elements to be visible if JS is enabled. That's where `yes-script` comes in.

The code is very simple, and can be found in the following files in this repo:

 * `custom-tag.html`: Use a custom HTML tag (`<yes-script>`). This is allowed as per the [custom elements](https://www.w3.org/TR/custom-elements/) spec, and is supported on [basically every](https://caniuse.com/custom-elementsv1) modern browser.
 * `using-class.html`: If you don't want to use a custom tag, then you can use a class (`class="yes-script"`) to enable the same functionality.


Usage:

```html
<head>

  <!-- include this in all your files where you want to use yes-script! -->
  <noscript>
    <style>
      yes-script {
        display: none !important;
      }
    </style>
  </noscript>

</head>

<body>

  <!-- the following will only show if JS is enabled -->
  <yes-script>
    JavaScript is enabled!
  </yes-script>

  <!-- the following will only show if JS is disabled -->
  <noscript>
    JavaScript is disabled!
  </noscript>

</body>
```
