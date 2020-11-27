# SmoothScroll
## Usage
`smoothScroll(to, duration)`
to : position like `200` or element id `'#home'`

### Example:
```html
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
  <style>
    html,
    body {
      margin: 0;
      height: 100%;
      overflow: hidden;
    }

    .navbar {
      position: sticky;
      margin: 2rem;
      top: 0;
      text-align: right;
    }

    .section {
      height: 50rem;
    }

    .to-top {
      position: fixed;
      bottom: 1rem;
      right: 1rem;
    }
  </style>
</head>

<body>
  <div style="height: 100%; overflow: auto;" id="element">
    <div class="navbar">
      <button onclick="scrollToElement(event, 0)">Home</button>
      <button onclick="scrollToElement(event, '#news')">News</button>
      <button onclick="scrollToElement(event, '#1500')">Description</button>
    </div>
    <h1 class="section" id="home">Home</h1>
    <h1 class="section" id="news">News</h1>
    <h1 class="section" id="1500">Description</h1>
    <button onclick="scrollToElement(event, 0)" class="to-top">To Top</button>
  </div>

  <script src="./smoothscroll.js"></script>

  <script>
    function scrollToElement(e, to) {
      e.preventDefault();
      // smoothScroll(scroll to, duration, element | default is window);
      smoothScroll(to, 800, document.getElementById("element"));
    }
  </script>
</body>

</html>
```
