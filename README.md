# Data Science Web Development

## Why do you need web development as a data scientist?
There are already good tools for data visualizing such as matplotlib, seaborn, or Tableau. However, there are cases where these tools are not sufficient enough.

For example, consider a project where you build a model that classifies disaster relief messages into categories. With your web development skills, you could turn that model into a web app where you would input a message and display the resulting message category.

## Bootstrap - Let's do the web development for you
Fortunately, if you are not used to web development there are great starter kits like Bootstrap. This is a easy to use front-end framework. Especially, CSS coding is simplified.

Here are some great Bootstrap links to get started:

- [Starter Template](https://getbootstrap.com/docs/4.0/getting-started/introduction/#starter-template)
- [Column Grid Explanation](https://getbootstrap.com/docs/4.0/layout/grid/)
- [Containers and Responsive Layout](https://getbootstrap.com/docs/4.0/layout/overview/)
- [Images](https://getbootstrap.com/docs/4.0/content/images/)
- [Navigation Bars](https://getbootstrap.com/docs/4.0/components/navbar/)
- [Font Colors](https://getbootstrap.com/docs/4.0/utilities/colors/)  

## The starter Template
Copy and paste the following code section into an index.html file and open the file in a browser.
```
<!doctype html>
<html lang="en">
  <head>
    <!-- Required meta tags -->
    <!-- Characters  used in the browser are UTF-8 -->
    <meta charset="utf-8">
    <!-- Shrinking the content for web vs. mobile -->
    <meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">

    <!-- Bootstrap CSS -->
    <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/css/bootstrap.min.css" integrity="sha384-Gn5384xqQ1aoWXA+058RXPxPg6fy4IWvTNh0E263XmFcJlSAwiGgFAW/dAiS6JXm" crossorigin="anonymous">

    <title>Hello, world!</title>
  </head>
  <body>
    <h1>ADD ROWS AND COLUMNS HERE</h1>
    <!-- row 1 -->
    <div class="row">
      <div class="col-1">C1</div>
    </div>

    <!-- row 2 -->
    <div class="row">
      <div class="col-1">C1</div>
    </div>

    <!-- Optional JavaScript -->
    <!-- jQuery first, then Popper.js, then Bootstrap JS -->
    <script src="https://code.jquery.com/jquery-3.2.1.slim.min.js" integrity="sha384-KJ3o2DKtIkvYIK3UENzmM7KCkRr/rE9/Qpg6aAZGJwFDMVNA/GpGFF93hXpG5KkN" crossorigin="anonymous"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.12.9/umd/popper.min.js" integrity="sha384-ApNbgh9B+Y1QKtv3Rn7W3mgPxhU9K/ScQsAP7hUibX39j7fakFPskvXusvfa0b4Q" crossorigin="anonymous"></script>
    <script src="https://maxcdn.bootstrapcdn.com/bootstrap/4.0.0/js/bootstrap.min.js" integrity="sha384-JZR6Spejh4U02d8jOt6vLEHfe/JQGiRRSQQxSfFWpi1MquVdAyjUar5+76PVCmYl" crossorigin="anonymous"></script>
  </body>
</html>
```
The important thing here already
- that the screen is divided in
  - 12 columns ()
  - as many columns as you need
- Behind the scene CSS is used to make the layout
- Just define (use special predefined) IDs and classes

#### Adding a row with 12 column C1...C12
```
<div class="row">
    <div class="col-1">C1</div>
    <div class="col-1">C2</div>
    <div class="col-1">C3</div>
    <div class="col-1">C4</div>
    <div class="col-1">C5</div>
    <div class="col-1">C6</div>
    <div class="col-1">C7</div>
    <div class="col-1">C8</div>
    <div class="col-1">C9</div>
    <div class="col-1">C10</div>
    <div class="col-1">C11</div>
    <div class="col-1">C12</div>
</div>
```
#### Adding one row with 2 columns (one column with 4 spaces an columns with 8 spaces)
```
<div class="row">
    <div class="col-4">C1</div>
    <div class="col-8">C2</div>
</div>
```

## Add a navigation bar
```

```

## Integrate Plotly plots

##
