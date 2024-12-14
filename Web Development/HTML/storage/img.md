# `<img>`
- It is a [[void element]].

```html
<!-- using relative url -->
<img src="images/dinosaur.jpg" alt="Dinosaur" />

<!-- using absolute url -->
<img src="https://www.example.com/images/dinosaur.jpg" alt="Dinosaur" />
```

***
## Attributes:
- `src` : url to the image
- `alt` : alternative text to display in place of the image in case the image did not get rendered because of some reason
```html
<img
  src="images/dinosaur.jpg"
  alt="The head and torso of a dinosaur skeleton;
          it has a large head with long sharp teeth"
/>
```

***
- We can use the `width` and `height` attributes to specify the width and height of our image.
- They are given as integers without a unit, and represent the image's width and height in pixels.
```html
<img
  src="images/dinosaur.jpg"
  width="400"
  height="341" 
/>
```

- There is a very good reason to do this.
- The HTML for your page and the image are separate resources, fetched by the browser as separate HTTP(S) requests. As soon as the browser has received the HTML, it will start to display it to the user. If the images haven't yet been received, then the browser will render only the HTML and will update the page with the image as soon as it is received.
![[Pasted image 20241126141217.png]]
- Take the above case in which the dev did not specify the height and width of the image.
- In this case, HTML will not know how much space to reserve for the image in the page, and therefore it will reserve none. It will adjust the text accordingly when the image arrives and is to be rendered. But this will frustrate the user who has already started reading the text.
- If you specify the height and width, the browser will know how much space to reserve for the image to be rendered.
![[Pasted image 20241126141506.png]]

***

*Reference:* [[raster vs vector images]]
