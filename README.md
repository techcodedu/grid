# Grid Exercise

Creating a Photo Collage and Text Section using HTML and CSS

In this guide, you will learn how to create a photo collage and text section using HTML and CSS. We will create a webpage with a text section on one side and a photo collage on the other side.

Here are the steps to create this webpage:

1. **Setup the HTML structure**

    Start by setting up the basic HTML structure. Include the `<!DOCTYPE html>`, `<html>`, `<head>`, and `<body>` tags.

    ```html
    <!DOCTYPE html>
    <html lang="en">
    <head>
        <meta charset="UTF-8" />
        <meta name="viewport" content="width=device-width, initial-scale=1.0" />
        <title>Document</title>
    </head>
    <body>
    </body>
    </html>
    ```

2. **Include the CSS**

    Inside the `<head>` tag, add the `<style>` tag to include the CSS.

    ```html
    <style>
    /* Add your CSS here */
    </style>
    ```

3. **Create the Container**

    Inside the `<body>` tag, create a container `<div>` with the class `section-container`.

    ```html
    <div class="section-container">
    </div>
    ```

    This container will hold the text section and the photo collage.

4. **Style the Container**

    Add the following CSS to style the `section-container`.

    ```css
    body {
        font-family: "Roboto", sans-serif;
    }

    .section-container {
        display: grid;
        grid-template-columns: 1fr 1fr;
        gap: 20px;
        max-width: 1080px;
        margin: auto;
        padding: 20px;
        box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        min-height: 500px;
    }
    ```

    This will create a grid container with two columns, each taking up half of the container's width. The `gap` is the space between the columns, and the `box-shadow` adds a shadow effect to the container.

5. **Create the Text Section**

    Inside the `section-container`, create a `<div>` with the class `text-section`. This will hold the text content.

    ```html
    <div class="text-section">
    </div>
    ```

6. **Style the Text Section**

    Add the following CSS to style the `text-section`.

    ```css
    .card {
        height: 300px;
        overflow: hidden;
        box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    }

    .card img {
        width: 100%;
        height: 100%;
        object-fit: cover;
    }

    .content {
        padding: 10px 0;
    }

    .content p {
        line-height: 1.5;
    }
    ```

    This will create a card with a height of 300px and a shadow effect. The `object-fit: cover;` will make the image cover the entire card while maintaining its aspect ratio. The `content` will have padding at the top and bottom, and the `<p>` tag will have a line-height of 1.5.

7. **Add Content to the Text Section**

    Inside the `text-section`, add a `card` `<div>` with an `<img>` tag, and a `content` `<div>` with a `<h2>` and `<p>` tag.

    ```html
    <div class="text-section">
        <div class="card">
            <img
            src="https://images.pexels.com/photos/18131916/pexels-photo-18131916/free-photo-of-city-fashion-man-people.jpeg"
            alt="Man in city"
            />
        </div>
        <div class="content">
            <h2>Heading</h2>
            <p>
            This is some short text. Lorem ipsum dolor sit amet, consectetur
            adipiscing elit. Quisque sodales, turpis vitae ullamcorper
            convallis, libero mauris scelerisque purus, at tempus tortor ligula
            ac tellus.
            </p>
        </div>
    </div>
    ```

8. **Create the Photo Collage**

    Next, create a `<div>` with the class `photo-collage` inside the `section-container`.

    ```html
    <div class="photo-collage">
    </div>
    ```

9. **Style the Photo Collage**

    Add the following CSS to style the `photo-collage`.

    ```css
    .photo-collage {
        display: grid;
        grid-template-columns: 1fr 2fr 1fr;
        grid-template-rows: 100px 100px 100px;
        gap: 5px;
    }

    .grid-item {
        height: 100px;
    }

    .grid-item img {
        width: 100%;
        height: 100%;
        object-fit: cover;
        box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        border-radius: 10px;
    }
    ```

    This will create a grid with three columns and three rows. The `gap` is the space between the grid items, and the `box-shadow` adds a shadow effect to the images. The `border-radius` adds rounded corners to the images.

10. **Add Images to the Photo Collage**

    Inside the `photo-collage`, add nine `grid-item` `<div>` with an `<img>` tag inside each one.

    ```html
    <div class="photo-collage">
        <div class="grid-item">
            <img
            src="https://images.pexels.com/photos/3567847/pexels-photo-3567847.jpeg"
            alt="Photo 1"
            />
        </div>
        <div class="grid-item" style="grid-column: 2 / 4">
            <img
            src="https://images.pexels.com/photos/3567847/pexels-photo-3567847.jpeg"
            alt="Photo 2"
            />
        </div>
        <div class="grid-item">
            <img
            src="https://images.pexels.com/photos/3567847/pexels-photo-3567847.jpeg"
            alt="Photo 3"
            />
        </div>
        <div class="grid-item" style="grid-row: span 2">
            <img
            src="https://images.pexels.com/photos/3567847/pexels-photo-3567847.jpeg"
            alt="Photo 4"
            />
        </div>
        <div class="grid-item" style="grid-row: span 2">
            <img
            src="https://images.pexels.com/photos/3567847/pexels-photo-3567847.jpeg"
            alt="Photo 5"
            />
        </div>
        <div class="grid-item" style="grid-column: span 2; grid-row: 2">
            <img


            src="https://images.pexels.com/photos/3567847/pexels-photo-3567847.jpeg"
            alt="Photo 6"
            />
        </div>
        <div class="grid-item" style="grid-column: 1; grid-row: 3">
            <img
            src="https://images.pexels.com/photos/3567847/pexels-photo-3567847.jpeg"
            alt="Photo 7"
            />
        </div>
        <div class="grid-item" style="grid-column: 1 / 3; grid-row: 3">
            <img
            src="https://images.pexels.com/photos/3567847/pexels-photo-3567847.jpeg"
            alt="Photo 8"
            />
        </div>
        <div class="grid-item" style="grid-column: 3; grid-row: 3">
            <img
            src="https://images.pexels.com/photos/3567847/pexels-photo-3567847.jpeg"
            alt="Photo 9"
            />
        </div>
    </div>
    ```

    The `grid-column` and `grid-row` styles are used to position the images in the grid.
