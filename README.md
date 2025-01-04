# goit-js-hw-08

Use this layout to style your task markup 

https://www.figma.com/design/m8k9NQV7qZrtYDCvxfD68B/HW-JavaScript?node-id=0-1&p=f&t=aW6eJhjD97xUevGz-0

Task — Image Gallery

Create a gallery with the ability to click on its elements and view a full-size image in a modal window. Watch the demo video of the gallery in action.

Creating a gallery is a complex task that is better broken down into smaller sub-tasks, each of which will bring you closer to the final goal. This process is called task decomposition.

1 - Gallery Markup
It makes sense to start by creating the container where we will add the gallery elements. For this, add the gallery container tag in the HTML code — an unordered list with the class gallery.

html
Копіювати код
<ul class="gallery"></ul>
2 - Image Array
To create the gallery elements, you will need data. Add this array of objects to your JavaScript file. Each object represents one gallery item.

preview — link to the small version of the image for the gallery card
original — link to the large version of the image for the modal window
description — textual description of the image, for the alt attribute of the small image and for the caption of the large image in the modal.
javascript
Копіювати код
const images = [
  {
    preview: 'https://cdn.pixabay.com/photo/2019/05/14/16/43/rchids-4202820__480.jpg',
    original: 'https://cdn.pixabay.com/photo/2019/05/14/16/43/rchids-4202820_1280.jpg',
    description: 'Hokkaido Flower',
  },
  // other image objects
];
3 - Gallery Item Markup
Now that you have the container where gallery elements can be added, and data to create them, it's time to fill the gallery with markup.

Use the images array and the HTML template for a gallery item. Create the markup for the elements in JavaScript and then add the entire markup inside ul.gallery. Do not add any other HTML tags apart from those contained in this template.

html
Копіювати код
<li class="gallery-item">
  <a class="gallery-link" href="large-image.jpg">
    <img
      class="gallery-image"
      src="small-image.jpg"
      data-source="large-image.jpg"
      alt="Image description"
    />
  </a>
</li>
In the src attribute of the <img> tag, specify the link to the small version of the image. Use the image description for the alt attribute. The link to the large image should be stored in the data-source attribute of the <img> element and specified in the href attribute of the link. Note that the image is wrapped in a link whose href attribute points to the path of the image file. So, clicking on it might trigger the download of the image to the user's computer. Prevent this behavior by default.

4 - Styling
Add styles for the gallery according to the provided layout.

5 - Event Delegation
Now it's time to add functionality for listening to clicks on the gallery elements and retrieving the link to the large image when clicked. Use event delegation on ul.gallery. For now, when clicking an element in the gallery, log the link to the large image in the console.

6 - Library Integration
The basicLightbox library provides a fully functional modal window that is perfect for our task. Use the CDN service from jsdelivr and add the links to the minified (.min) JS and CSS files of the library in your HTML file.

7 - Modal Window
Enhance your code so that when a gallery item is clicked, the modal window from the basicLightbox library opens. To learn how to initialize the modal window in your code and how to use it, refer to the library documentation and examples.

8 - Large Image
Use your code for retrieving the link to the large image to replace the src attribute of the <img> element in the modal window before it opens. Use the ready-made modal markup from the basicLightbox library examples.

Mentor’s Focus During Review:
The live page displays a gallery of images from the images data array.
The image gallery is styled according to the layout.
Gallery data is dynamically created in JavaScript.
Event delegation is used for listening to click events on gallery items.
When clicking between gallery items, nothing happens by default.
The basicLightbox library is integrated.
When a gallery item is clicked, the modal window from the integrated library opens, showing the enlarged version of the clicked image.
