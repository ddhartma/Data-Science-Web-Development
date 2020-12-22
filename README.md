[image1]: web_layout.png "web_layout"
[image2]: navbar.png "navbar"
# Data Science Web Development

Let`s create an interactive Data Science Dashboard.

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


## The two project folders in this repo:
There are two project folders in this Project
- web_app: This folder contains all files as described below
- web_app_empty_template: Is a completely empty template for own developments

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


## How to use jQuery
This is just a simple introduction.

Jquery is a JavaScript library that makes developing the front-end easier. The Bootstrap library depends on jQuery.
Here is a link to the documentation of the core functions in jQuery: [jQuery API documentation](https://api.jquery.com/)
There are newer JavaScript tools out there like [React](https://reactjs.org/) and [Angular](https://angularjs.org/).


The jQuery code is more intuitive. Once the document has loaded, the following code adds an onclick event to the image. Once the image is clicked, the h1 tag's text is changed.
```
$(document).ready(function(){
    $("img").click(function(){
        $("h1").text("A Photo of a Breathtaking View");
    });
});
```

- The dollar sign $ is jQuery syntax that says "grab this element, class or id" (similar to CSS).
- For example $("p#first") means find the paragraph with id="first". Or $("#first") would work as well.
- The ready() function waits for the html document to load. Then there is another function being passed into the ready function. This section function adds an on-click event to an image tag. Then there's another function passed into the click() function, which changes the h1 text.


## Integrate Plotly plots
[Plotly](), although a private company, provides open source libraries for both JavaScript and Python.

Here are a few links to some helpful parts of the plotly documentation:
- [javascript examples](https://plot.ly/javascript/)
- [getting started](https://plot.ly/javascript/getting-started/)
- [linking to the plotly library](https://plot.ly/javascript/getting-started/#plotlyjs-cdn)

#### How to use it?
1. Set a link the javascript source file in the header section of the html file:
```
<script src="https://cdn.plot.ly/plotly-latest.min.js"></script>
```

2. Create a div with the plotly id and a script with the source file

  2.1 The Javascript Version

  in the index.html file add:

  ```
  <div class="col-6">
      <div id="plot1"></div>
  </div>
  <script src="Plot1.js"></script>
  ```

  ```
  <div class="col-6">
      <div id="plot2"></div>
  </div>
  <script src="Plot2.js"></script>
  ```

  Plot1.js (scatter plot):

  ```
  var year = [1995, 1996, 1997, 1998, 1999, 2000, 2001, 2002, 2003, 2004, 2005,
       2006, 2007, 2008, 2009, 2010, 2011, 2012, 2013, 2014, 2015];

  var arable_land_brazil = [30.924583699244103,
   30.990028882024003,
   31.0554740648039,
   31.1207996037396,
   31.198209170939897,
   31.275618738140302,
   31.521965413357503,
   31.8094695709811,
   32.1206632097572,
   32.558918611078504,
   32.5948835506464,
   32.6369263974999,
   32.4998145520415,
   32.7225913899504,
   32.7273771437186,
   32.7181645677148,
   32.9466843101456,
   32.974680969689395,
   33.3576728793727,
   33.8100342899258,
   33.8100342899258];

  var country_name_brazil = 'Brazil';

  var trace1 = {
    x:year,
    y:arable_land_brazil,
    mode:'lines',
    type:'scatter',
    name:country_name_brazil
  };

  var arable_land_germany = [49.67917502148379,
   49.6634105817984,
   49.6404526572124,
   49.776517105037,
   49.1489483638031,
   48.912451640636206,
   48.822012037833204,
   48.6355558103537,
   48.7400017201342,
   48.7799982796686,
   48.8330083725198,
   48.5948612066988,
   48.61330197608051,
   48.535696870607794,
   48.4380826711798,
   47.9100324181656,
   47.9659169153087,
   47.8108681930338,
   47.8588626461821,
   47.9363714531384,
   47.9592041483809];

  var country_name_germany = 'Germany';

  var trace2 = {
    x:year,
    y:arable_land_germany,
    mode:'lines',
    type:'scatter',
    name:country_name_germany,
  };

  var data = [trace1, trace2];
  Plotly.newPlot('plot1', data, layout);
  ```

  plot2.js (bar plot):

  ```
  var year = [2015];
  var arable_land_brazil = [33.8100342899258];
  var country_name_brazil = 'Brazil';

  var arable_land_germany = [47.9592041483809];
  var country_name_germany = 'Germany';

  var arable_land_china = [56.2229587724434];
  var country_name_china = 'China';

  var trace1 = {
    x: [country_name_brazil, country_name_germany, country_name_china],
    y: [arable_land_brazil[0], arable_land_germany[0], arable_land_china[0]],
    type: 'bar'
  };

  var layout = {
   title: 'Percent of Land Area Used for <br> Agriculture in 2015'
  };

  var data = [trace1];

  Plotly.newPlot('plot2', data, layout);
  ```

  2.2 The Python Version (wrangle_data.py)

  in the index.html add:

  ```
  <div class="col-6">
      <div id="{{ids[0]}}"></div>
  </div>
  ```
  ```
  <div class="col-6">
      <div id="{{ids[1]}}"></div>
  </div>
  ```

  Scatter Plot

  ```
  # first chart plots arable land from 1990 to 2015 in top 10 economies
  # as a line chart

  graph_one = []
  df = cleandata('data/API_AG.LND.ARBL.HA.PC_DS2_en_csv_v2.csv')
  df.columns = ['country','year','hectaresarablelandperperson']
  df.sort_values('hectaresarablelandperperson', ascending=False, inplace=True)
  countrylist = df.country.unique().tolist()

  for country in countrylist:
      x_val = df[df['country'] == country].year.tolist()
      y_val =  df[df['country'] == country].hectaresarablelandperperson.tolist()
      graph_one.append(
          go.Scatter(
          x = x_val,
          y = y_val,
          mode = 'lines',
          name = country
          )
      )

  layout_one = dict(title = 'Change in Hectares Arable Land <br> per Person 1990 to 2015',
              xaxis = dict(title = 'Year',
              autotick=False, tick0=1990, dtick=25),
              yaxis = dict(title = 'Hectares'),
              )

  ```

  Bar Plot

  ```
  # second chart plots ararble land for 2015
  # as a bar chart    

  graph_two = []
  df = cleandata('data/API_AG.LND.ARBL.HA.PC_DS2_en_csv_v2.csv')
  df.columns = ['country','year','hectaresarablelandperperson']
  df.sort_values('hectaresarablelandperperson', ascending=False, inplace=True)
  df = df[df['year'] == 2015]

  graph_two.append(
    go.Bar(
    x = df.country.tolist(),
    y = df.hectaresarablelandperperson.tolist(),
    )
  )

  layout_two = dict(title = 'Hectares Arable Land per Person in 2015',
              xaxis = dict(title = 'Country',),
              yaxis = dict(title = 'Hectares per person'),
              )

  ```

  Append figures to a figures list

  ```
  # append all charts to the figures list
  figures = []
  figures.append(dict(data=graph_one, layout=layout_one))
  figures.append(dict(data=graph_two, layout=layout_two))
  ```

#### Other options
- [d3.js](https://d3js.org/) is one of the most popular (and complex!) javascript data visualization libraries. This library is still actively being developed.
- Other options include [chart.js](https://classroom.udacity.com/nanodegrees/nd025/parts/0469f04b-1440-4b2c-9f69-8882d6ec436b/modules/237f5e87-7a8e-49d1-aab9-241006ce715e/lessons/3737ebcb-984e-4959-bf2a-95fe13de4916/concepts/ww.chartjs.org/), [Google Charts](https://developers.google.com/chart/), and [nvd3.js](nvd3.org/), which is built on top of d3.js

## Flask

[Flask](flask.pocoo.org/) - a web framework takes care of all the routing needed to organize a web page

#### File top start the web app - worldbank.py file
This file starts the web app server
```
from worldbankapp import app
app.run(host='0.0.0.0', port=3001, debug=True)
```

#### The worldbankapp folder
- Here is the template folder with the ```ìndex.html``` file inside
- The ```__init__.py```
  ```
  from flask import Flask
  app = Flask(__name__)
  from worldbankapp import routes
  ```
  - Flask is setup as a python package
  - When the package is run, the init file gets run first
  - It imports Flask, creates a variable called app and finally imports the routes file

- the routes.py file to create a new page

#### Create a new page
To create a new web page, you first need to specify the route in the routes.py as well as the name of the html template.

```
@app.route('/new-route')
def render_the_route():
    return render_template('new_route.html')
```

#### To start the server type in the Terminal

```
python worldbank.py
```

Get Domain and ID

```
env | grep WORK
```

This will return the necessary info

```
WORKSPACEDOMAIN=udacity-student-workspaces.com
WORKSPACEID=viewc7f3319f2
```

The web page is located at

```
http://WORKSPACEID-3001.WORKSPACEDOMAIN
```

## How does Panda, Plotly, Flask and HTML work together?
1. Plotly installation
  ```
  pip install Plotly
  ```

#### wrangle_data.py

2. The data is loaded in ```/wrangling_scripts/wrangle_data.py``` file via
  ```
  df = pd.read_csv(dataset, skiprows=4)
  ```
3. The data has to be cleaned there

#### routes.py

4. Import Plotly in ```routes.py```
  ```
  from worldbankapp import app
  import json, plotly
  from flask import render_template
  from wrangling_scripts.wrangle_data import return_figures
  ```

5. The data is returned to ```routes.py```file via
  ```
  data = data_wrangling()
  ```

6. get figures from wrangle_data.py via
  ```
  figures = return_figures()
  ```

7. Create ids as a list
  ```
  ids = ['figure-{}'.format(i) for i, _ in enumerate(figures)]
  ```

10. Convert the plotly figures to JSON for javascript in html template
  ```
  figuresJSON = json.dumps(figures, cls=plotly.utils.PlotlyJSONEncoder)
  ```

11. Via the ```render_template``` function the data is sent from the backend to the frontend
  ```
  @app.route('/')
  @app.route('/index')
  def index():
      return render_template('index.html',
                            data_set = data,
                            ids=ids,
                            figuresJSON=figuresJSON)
  ```

#### index.html
12. In the index.html file, the ```data_set``` variable and ```figuresJSON``` can be accessed by using a template engine called [Jinja](https://jinja.palletsprojects.com/en/2.11.x/):
  ```
  <p>{{ data_set }}</p>
  ```
  similar
  ```
  <p>{{ ids }}</p>
  <p>{{ figuresJSON }}</p>
  ```
  and to get the Plotlys add ids like shown above
  ```
  <div class="col-6">
      <div id="{{ ids[0] }}"></div>
  </div>
  ```
  and add the following code block at the end of index.html
  ```
  <script type="text/javascript">
    // plots the gigures with id

    var figures = {{ figuresJSON | safe }};
    var ids = {{ ids | safe }}
    for(var i in figures) {
      Plotly.plot(ids[i]),
      figures[i].data,
      figures[i].layout || {});
    }
  </script>
  ```

## Setup Instructions

The following is a brief set of instructions on setting up a cloned repository.

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

### Prerequisites: Installation of Python via Anaconda and Command Line Interaface
- Install [Anaconda](https://www.anaconda.com/distribution/). Install Python 3.7 - 64 Bit
- If you need a good Command Line Interface (CLI) under Windowsa you could use [git](https://git-scm.com/). Under Mac OS use the pre-installed Terminal.

- Upgrade Anaconda via
```
$ conda upgrade conda
$ conda upgrade --all
```

- Optional: In case of trouble add Anaconda to your system path. Write in your CLI
```
$ export PATH="/path/to/anaconda/bin:$PATH"
```

### Clone the project
- Open your Command Line Interface
- Change Directory to your project older, e.g. `cd my_github_projects`
- Clone the Github Project inside this folder with Git Bash (Terminal) via:
```
$ git clone https://github.com/ddhartma/Data-Science-Web-Development.git
```

- Change Directory
```
$ cd 3_Flask
```

- Create a new Python environment, e.g. ds_dashboard. Inside Git Bash (Terminal) write:
```
$ conda create --name ds_dashboard
```

- Install the following packages (via pip or conda)
```
numpy = 1.17.4
pandas = 0.24.2
plotly = 4.6.0
Flask = 1.1.2
```

- Check the environment installation via
```
$ conda env list
```

- Activate the installed spotify_analysis environment via
```
$ conda activate ds_dashboard
```
