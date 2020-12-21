[image1]: web_layout.png "web_layout"
[image2]: navbar.png "navbar"
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
    <h1>Let's build a Data Science Web App</h1>

    <!-- navbar -->
    <nav ...>
    ...
    </nav>

    <!-- rows and columns -->
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
#### Create an example with
- col-1 (1 space - left column with github, linkedin)
- col-11 (11 space - for two rows and two columns for 4 Plotly plots)

```
<!--middle section-->
<div class="row">

    <!--social media buttons column-->
    <div class="col-1 border-right">
        <div id="follow-me" class="mt-3">
            <a href="#">
                <img src="../static/img/linkedinlogo.png" alt="linkedin" class="img-fluid mb-4 ml-2">
            </a>
            <a href="#">
                <img src="../static/img/githublogo.png" alt="github" class="img-fluid ml-2">
            </a>
        </div>
    </div>

    <!--visualizations column-->
    <div class="col-11">

        <!--chart descriptions-->
        <div id="middle-info" class="mt-3">

            <h2 id="tag-line">World Bank Data Dashboard</h2>
            <h4 id="tag-line" class="text-muted">Top 10 World Economies Land Use</h4>

        </div>

        <!--Plotly charts-->
        <div id="charts" class="container mt-3 text-center">

            <!--top two charts-->
            <div class="row">
                <div class="col-6">
                    <div id="{{ids[0]}}"></div>
                </div>
                <div class="col-6">
                    <div id="{{ids[1]}}"></div>
                </div>
            </div>

            <!--bottom two charts-->
            <div class="row mb-6">
                <div class="col-6">
                    <div id="chart3">
                        <div id="{{ids[2]}}"></div>
                    </div>
                </div>
                <div class="col-6">
                    <div id="chart4">
                        <div id="{{ids[3]}}"></div>
                    </div>
                </div>
            </div>

            <!--Create another row and place a fifth chart in that row-->
            <div class="row mb-6">
              <div class="col-12">
                <div id="chart5">
                    <div id="{{ids[4]}}"></div>
                </div>
              </div>
            </div>

        </div>
    <div>
</div>
```
- to add a border for the follow me images add ```<div class="col-1 border-right">```
- add margin-top of 3px via ```<div class=mt-3>```
- add margin-left of 2px via ```<div class=ml-2>```
- add margin-bottom of 4px via ```<div class=mb-4>```
- use ```class="img-fluid"``` to enlarge and shrink images automatically depending on screen size
- use ```class="text-muted"``` to change text color to gray

#### Image of the web Layout

![web_layout][image1]

## Add a navigation bar (example)
```
<!--navbar links-->     
<nav class="navbar navbar-expand-lg navbar-dark bg-dark sticky-top">
   <a class="navbar-brand" href="#">World Bank Dashboard</a>
  <button class="navbar-toggler" type="button" data-toggle="collapse"
  data-target="#navbarTogglerDemo02"
  aria-controls="navbarTogglerDemo02" aria-expanded="false"
  aria-label="Toggle navigation">
    <span class="navbar-toggler-icon"></span>
  </button>

  <div class="collapse navbar-collapse" id="navbarTogglerDemo02">
    <ul class="navbar-nav ml-auto mt-2 mt-lg-0">
      <li class="nav-item">
        <a class="nav-link" href="https://www.udacity.com">Udacity</a>
      </li>
      <li class="nav-item">
        <a class="nav-link" href="https://data.worldbank.org/">World Bank Data</a>
      </li>
    </ul>
  </div>
</nav>
```

#### Style color of navbar
```
<nav class="navbar navbar-expand-lg navbar-dark bg-dark sticky-top">
```
  - navbar-dark (or e.g. navbar-light)
  - bg-dark (or e.g. bg-light)

#### Add navbar items via

```
<li class="nav-item">
    <a class="nav-link" href="https://www.udacity.com">Udacity</a>
</li>
```

#### Align the navbar to the right screen side
```
<ul class="navbar-nav ml-auto mt-2 mt-lg-0">
```
use ml-auto to auto align the navbar to the right side

#### Image of the navbar
![navbar][image2]

## Integrate Plotly plots

##
