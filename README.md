
<!DOCTYPE html>
<html>
<head>

  <meta http-equiv="Content-Type" content="text/html; charset=utf-8"/>  <script type="application/shiny-singletons"></script>  <script type="application/html-dependencies">json2[2014.02.04];jquery[1.12.4];babel-polyfill[6.7.2];shiny[0.14.2];selectize[0.11.2];bootstrap[3.3.7]</script><script src="shared/json2-min.js"></script>
<script src="shared/jquery.min.js"></script>
<script src="shared/babel-polyfill.min.js"></script>
<link href="shared/shiny.css" rel="stylesheet" />
<script src="shared/shiny.min.js"></script>
<link href="shared/selectize/css/selectize.bootstrap3.css" rel="stylesheet" />
<!--[if lt IE 9]>
<script src="shared/selectize/js/es5-shim.min.js"></script>
<![endif]-->
<script src="shared/selectize/js/selectize.min.js"></script>
<meta name="viewport" content="width=device-width, initial-scale=1" />
<link href="shared/bootstrap/css/bootstrap.min.css" rel="stylesheet" />
<script src="shared/bootstrap/js/bootstrap.min.js"></script>
<script src="shared/bootstrap/shim/html5shiv.min.js"></script>
<script src="shared/bootstrap/shim/respond.min.js"></script>  <title></title>
  <title>The relationship between variables and miles per gallon (MPG)</title>

</head>

<body>
  <nav class="navbar navbar-default navbar-static-top" role="navigation">
    <div class="container">
      <div class="navbar-header">
        <span class="navbar-brand"></span>
      </div>
      <ul class="nav navbar-nav">
        <li class="active">
          <a href="#tab-7769-1" data-toggle="tab" data-value="Detail">Detail</a>
        </li>
        <li>
          <a href="#tab-7769-2" data-toggle="tab" data-value="Analysis">Analysis</a>
        </li>
      </ul>
    </div>
  </nav>
  <div class="container-fluid">
    <div class="tab-content">
      <div class="tab-pane active" data-value="Detail" id="tab-7769-1">
        <h2>Motor Trend</h2>
        <hr/>
        <h3>Description</h3>
        <span class="help-block">
          The data was extracted from the 1974 Motor Trend US magazine,
           and comprises fuel consumption and 10 aspects of automobile design and performance
           for 32 automobiles (1973-74 models).
        </span>
        <h3>Format</h3>
        <p>A data frame with 32 observations on 11 variables.</p>
        <p>  [, 1]   mpg	 Miles/(US) gallon</p>
        <p>  [, 2]	 cyl	 Number of cylinders</p>
        <p>  [, 3]	 disp	 Displacement (cu.in.)</p>
        <p>  [, 4]	 hp	 Gross horsepower</p>
        <p>  [, 5]	 drat	 Rear axle ratio</p>
        <p>  [, 6]	 wt	 Weight (lb/1000)</p>
        <p>  [, 7]	 qsec	 1/4 mile time</p>
        <p>  [, 8]	 vs	 V/S</p>
        <p>  [, 9]	 am	 Transmission (0 = automatic, 1 = manual)</p>
        <p>  [,10]	 gear	 Number of forward gears</p>
        <p>  [,11]	 carb	 Number of carburetors</p>
        <h3>Source</h3>
        <p>Henderson and Velleman (1981), Building multiple regression models interactively. Biometrics, 37, 391-411.</p>
      </div>
      <div class="tab-pane" data-value="Analysis" id="tab-7769-2">
        <div class="container-fluid">
          <h2>The relationship between variables and miles per gallon (MPG)</h2>
          <div class="row">
            <div class="col-sm-4">
              <form class="well">
                <div class="form-group shiny-input-container">
                  <label class="control-label" for="variable">Variable:</label>
                  <div>
                    <select id="variable"><option value="cyl" selected>Number of cylinders</option>
<option value="disp">Displacement (cu.in.)</option>
<option value="hp">Gross horsepower</option>
<option value="drat">Rear axle ratio</option>
<option value="wt">Weight (lb/1000)</option>
<option value="qsec">1/4 mile time</option>
<option value="vs">V/S</option>
<option value="am">Transmission</option>
<option value="gear">Number of forward gears</option>
<option value="carb">Number of carburetors</option></select>
                    <script type="application/json" data-for="variable" data-nonempty="">{}</script>
                  </div>
                </div>
                <div class="form-group shiny-input-container">
                  <div class="checkbox">
                    <label>
                      <input id="outliers" type="checkbox"/>
                      <span>Show BoxPlot's outliers</span>
                    </label>
                  </div>
                </div>
              </form>
            </div>
            <div class="col-sm-8">
              <h3>
                <div id="caption" class="shiny-text-output"></div>
              </h3>
              <div class="tabbable">
                <ul class="nav nav-tabs">
                  <li class="active">
                    <a href="#tab-8075-1" data-toggle="tab" data-value="BoxPlot">BoxPlot</a>
                  </li>
                  <li>
                    <a href="#tab-8075-2" data-toggle="tab" data-value="Regression model">Regression model</a>
                  </li>
                </ul>
                <div class="tab-content">
                  <div class="tab-pane active" data-value="BoxPlot" id="tab-8075-1">
                    <div id="mpgBoxPlot" class="shiny-plot-output" style="width: 100% ; height: 400px"></div>
                  </div>
                  <div class="tab-pane" data-value="Regression model" id="tab-8075-2">
                    <div id="mpgPlot" class="shiny-plot-output" style="width: 100% ; height: 400px"></div>
                    <pre id="fit" class="shiny-text-output"></pre>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</body>

</html>
