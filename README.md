# PDF Flipbook Viewer

A beautiful and interactive PDF flipbook viewer that transforms your PDF documents into a realistic book-like reading experience with page-turning animations and intuitive controls. Originally set up by [LibFi.io](https://libfi.io) and released under the MIT license.

## Features

- 3D page-turning animations with WebGL support
- Responsive design that works on desktop and mobile devices
- Touch-enabled for mobile devices
- Customizable UI controls and appearance
- PDF navigation and zoom functionality
- Support for both single and double-page viewing modes
- Sound effects for page turns (optional)
- Cross-browser compatibility
- SEO-friendly with customizable meta tags

## Setup

1. Clone this repository or download the files
2. Place your PDF file in the root directory
3. Update the `index.html` file with your PDF filename
4. Configure your page title, meta tags, and preview image

### SEO and Preview Setup

Update the following sections in your `index.html` file:

```html
<!-- Page Title -->
<title>Your PDF Title Here</title>

<!-- SEO Meta Tags -->
<meta name="description" content="Your PDF description here">
<meta name="keywords" content="relevant, keywords, here">
<meta name="author" content="Your Name">

<!-- Site Preview Tags -->
<meta name="thumbnail" content="https://your-domain.com/preview.png" />
<link rel="image_src" href="https://your-domain.com/preview.png" />

<!-- Open Graph Meta Tags for Social Media -->
<meta property="og:title" content="Your PDF Title">
<meta property="og:description" content="Your PDF description">
<meta property="og:type" content="website">
<meta property="og:url" content="https://your-domain.com">
<meta property="og:image" content="https://your-domain.com/preview.png">
<meta property="og:image:width" content="1200">
<meta property="og:image:height" content="630">

<!-- Twitter Card Meta Tags -->
<meta name="twitter:card" content="summary_large_image">
<meta name="twitter:title" content="Your PDF Title">
<meta name="twitter:description" content="Your PDF description">
<meta name="twitter:image" content="https://your-domain.com/preview.png">
```

### Preview Image Requirements

- Create a preview image (recommended size: 1200x630 pixels)
- Save it as `preview.png` in the root directory
- Ensure the image is web-optimized (compressed)
- Use a clear, representative image of your PDF content

## Usage

### Basic Setup

The minimum setup requires including the necessary CSS and JavaScript files, and initializing the flipbook with jQuery:

```html
<!-- Include required CSS -->
<link href="lib/css/main.css" rel="stylesheet">
<link href="lib/css/themify-icons.min.css" rel="stylesheet">

<!-- Create a container for the flipbook -->
<div id="flipbookContainer"></div>

<!-- Include required JavaScript -->
<script src="lib/js/libs/jquery.min.js"></script>
<script src="lib/js/flip.js"></script>

<!-- Initialize the flipbook -->
<script>
jQuery(document).ready(function() {
    var pdf = 'your-pdf-file.pdf';
    var options = {
        height: 2000,
        duration: 700,
        backgroundColor: "#2F2D2F"
    };
    var flipBook = $("#flipbookContainer").flipBook(pdf, options);
});
</script>
```

### Configuration Options

The flipbook can be customized with various options:

```javascript
var options = {
    height: 2000,                    // Height of the flipbook container
    duration: 700,                   // Page turn animation duration in milliseconds
    backgroundColor: "#2F2D2F",      // Background color
    soundEnable: false,              // Enable/disable page turn sound
    useTouch: true,                  // Enable touch support
    pageMode: FLIP.PAGE_MODE.AUTO,   // Page mode (SINGLE, DOUBLE, AUTO)
    autoPlay: false,                 // Auto flip pages
    autoPlayDuration: 5000,          // Duration between auto flips
    webgl: true                      // Enable/disable WebGL rendering
};
```

## Directory Structure

```
├── lib/
│   ├── css/
│   │   ├── main.css
│   │   └── themify-icons.min.css
│   └── js/
│       ├── flip.js
│       └── libs/
│           ├── jquery.min.js
│           ├── pdf.min.js
│           ├── pdf.worker.min.js
│           └── three.min.js
├── index.html
└── your-pdf-file.pdf
```

## Browser Support

- Chrome (recommended)
- Firefox
- Safari
- Edge
- Internet Explorer 11

## Dependencies

- jQuery
- PDF.js
- Three.js (for WebGL rendering)

## License

MIT License

Copyright (c) 2024 Liberty Finance

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
