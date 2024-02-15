[SVG](https://developer.mozilla.org/en-US/docs/Web/SVG){: target="_blank"} (Scalable Vector Graphics) has a similar syntax as HTML. They are both based on XML. Since [HTML5](https://en.wikipedia.org/wiki/HTML5){: target="_blank"} we can simply inline the code of an SVG image inside an HTML file like below.

```svg
<html>
  <h1>Hi there</h1>
  <svg width="100" height="100" viewBox="0 0 100 100">
    <circle cx="50" cy="50" r="25" fill="red" />
  </svg>
</html>
```

This opens up a lot of cool options. We can access parts of an image with JavaScript to make something interactive, or we can generate art with code. We can also move some styling to CSS and animate image elements with CSS.

In this tutorial series, we learn the foundations of the SVG syntax step by step from basic to more advanced topics.
