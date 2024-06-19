Improving the accessibility of HTML involves adopting best practices that ensure web content is usable by people with various disabilities. Here are three ways to enhance the accessibility of HTML:

### 1. Use Semantic HTML Elements
Semantic HTML elements provide meaningful context to both browsers and assistive technologies, making it easier for users to navigate and understand the content.

- **Example**: Use `<header>`, `<nav>`, `<main>`, `<article>`, `<section>`, and `<footer>` instead of generic `<div>` and `<span>` elements.
- **Benefit**: Improves the structure and readability of the content for screen readers and other assistive technologies.

```html
<header>
  <h1>Website Title</h1>
  <nav>
    <ul>
      <li><a href="#home">Home</a></li>
      <li><a href="#about">About</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>
  </nav>
</header>
<main>
  <article>
    <h2>Article Title</h2>
    <p>Content of the article...</p>
  </article>
</main>
<footer>
  <p>© 2024 Your Website</p>
</footer>
```

### 2. Provide Text Alternatives for Non-Text Content
Text alternatives (alt text) for images, videos, and other non-text content help users who rely on screen readers to understand the content.

- **Example**: Use the `alt` attribute for images and provide transcripts or captions for audio and video content.
- **Benefit**: Ensures that all users, including those with visual and auditory impairments, can access and understand the content.

```html
<img src="example.jpg" alt="Description of the image">
<video controls>
  <source src="example.mp4" type="video/mp4">
  <track kind="captions" src="captions.vtt" srclang="en" label="English">
  Your browser does not support the video tag.
</video>
```

### 3. Ensure Keyboard Accessibility
Ensuring that all interactive elements (links, buttons, form controls) can be accessed and operated using a keyboard is crucial for users with motor disabilities who cannot use a mouse.

- **Example**: Use proper HTML elements for buttons and links, and manage focus appropriately.
- **Benefit**: Enhances the usability of the web page for users who rely on keyboard navigation.

```html
<a href="example.html" class="button">Click Here</a>
<button type="button">Submit</button>

<!-- Ensure focus management in JavaScript -->
<button id="openModal">Open Modal</button>
<div id="modal" role="dialog" aria-hidden="true">
  <button id="closeModal">Close</button>
  <!-- Modal content -->
</div>

<script>
  document.getElementById('openModal').addEventListener('click', function() {
    document.getElementById('modal').setAttribute('aria-hidden', 'false');
    document.getElementById('closeModal').focus();
  });

  document.getElementById('closeModal').addEventListener('click', function() {
    document.getElementById('modal').setAttribute('aria-hidden', 'true');
    document.getElementById('openModal').focus();
  });
</script>
```

By following these practices, you can significantly improve the accessibility of your HTML content, making it more inclusive for users with disabilities.