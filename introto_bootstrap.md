
###Bootstrap

Developers like yourself create code. Designers make the interface look nice. But not every project has a designer. Sometimes that job is also yours. Congratulations!

You have a secret weapon. Bootstrap is the most popular HTML, CSS, and JS framework for developing responsive, mobile first projects on the web. Bootstrap is a framework. It uses  html, cascading style sheets and javascript. Bootstrap contains design templates for typography, forms, buttons, navigation and other interface components. 

Bootstrap allows you to create responsive web pages. Responsive web design provides optimal viewing and interaction experience on all devices. Without responsive design you would develop different pages for different devices. Bootstrap solves that problem and ends the madness.

The place to get started for Bootstrap is http://getbootstrap.com/. So if you have any questions about Bootstrap try that site first.

####Including Bootstrap in your JSP or HTML Page

You can download the Bootstrap libraries to your computer and link to them. Or, you could  take the easy route and link to a hosted version at a Content Delivery Network. We'll link to the hosted version. Include three links in your web page as shown below. Place the links just before the ending ```</head>``` tag.

{%ace edit=false, lang='html'%}
<!-- Latest compiled and minified CSS -->
<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.6/css/bootstrap.min.css" integrity="sha384-1q8mTJOASx8j1Au+a5WDVnPi2lkFfwwEAa8hDDdjZlpLegxhjVME1fgjWPGmkzs7" crossorigin="anonymous">

<!-- Optional theme -->
<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.6/css/bootstrap-theme.min.css" integrity="sha384-fLW2N01lMqjakBkx3l/M9EahuwpSfeNvV63J5ezn3uZzapT0u7EYsXMjQV+0En5r" crossorigin="anonymous">

<!-- Latest compiled and minified JavaScript -->
<script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.6/js/bootstrap.min.js" integrity="sha384-0mSbJDEHialfmuBBQP6A4Qrprq5OVfW37PRR3j5ELqxss1yVqOtnepnHVP9aJ7xS" crossorigin="anonymous"></script>
{%endace%}

<div style="page-break-after: always;"></div>
####A basic Bootstrap page
To create a basic Bootstrap page

{%ace edit=false, lang='html'%}
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <!-- The above 3 meta tags *must* come first in the head; any other head content must come *after* these tags -->
    <title>Bootstrap 101 Template</title>

    <!-- Bootstrap -->
    <link href="css/bootstrap.min.css" rel="stylesheet">

    <!-- HTML5 shim and Respond.js for IE8 support of HTML5 elements and media queries -->
    <!-- WARNING: Respond.js doesn't work if you view the page via file:// -->
    <!--[if lt IE 9]>
      <script src="https://oss.maxcdn.com/html5shiv/3.7.2/html5shiv.min.js"></script>
      <script src="https://oss.maxcdn.com/respond/1.4.2/respond.min.js"></script>
    <![endif]-->
    <!-- jQuery (necessary for Bootstrap's JavaScript plugins) -->
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/1.11.3/jquery.min.js"></script>
    <!-- Include all compiled plugins (below), or include individual files as needed -->
    <script src="js/bootstrap.min.js"></script>
  </head>
  <body>
   
  </body>
</html>
{%endace%}

Next, add a navigation bar to your page. Put it right below the body tag. Now users of your website won't get lost.

{%ace edit=false, lang='html'%}
<div class="navbar navbar-default navbar-static-top" role="navigation">
    <div class="container">
        <div class="navbar-header">
            <button type="button" class="navbar-toggle" data-toggle="collapse" data-target=".navbar-collapse">
            <span class="sr-only">Toggle navigation</span>
            <span class="icon-bar"></span>
            <span class="icon-bar"></span>
            <span class="icon-bar"></span>
            </button>
            <a class="navbar-brand" href="http://mikspot.com/" title='Your choice, your world!'>Home</a>
        </div>
 
        <div class="navbar-collapse collapse">
            <ul class="nav navbar-nav">
                <li class="active">
                    <a href="#">All</a>
                </li>
                <li>
                    <a href="#">Demo</a>
                </li>
                <li>
                    <a href="#">Contact</a>
                </li>
            </ul>
        </div><!--/.nav-collapse -->
 
    </div>
</div>
{%endace%}

You need a another ```<div>``` tag below the navigation bar to denote the page container. 
The container class sets the content's margins. This keeps the content together as screen size changes. The container class creates 'boxed' contents of your Bootstrap page.

Note: You don't want a container inside a container since nesting containers is not the goal. Having multiple containers is fine. You may wish to wrap the entire contents inside one container. Suit yourself.

{%ace edit=false, lang='html'%}
<div class="container">
 
</div>
{%endace%}

Add a Heading. But not just any heading. We're going to create a Jumbotron heading. Let them know we're here!

