# Responsive Bootstrap Tab / Pills To Navbar Demo
A responsive demo for @twitter bootstrap, when device is lager then tablets, you will see Tab or Pills, when smaller you will see Navbar.

To see demo: http://wellwind.github.io/bootstrap-responsive-tab-pills-to-navbar.html

## How To Use

### Step1. Wrap a div with class name responsive-nav-tabs2bar/responsive-nav-pills2bar to navigation code
```HTML
<div id="top_menu" class="responsive-nav-tabs2bar">
  <nav class="navbar navbar-default" role="navigation">
    <div class="container-fluid">
      <!-- Brand and toggle get grouped for better mobile display -->
      <div class="navbar-header">
        <button type="button" class="navbar-toggle collapsed" data-toggle="collapse" data-target="#bs-example-navbar-collapse-1">
          <span class="sr-only">Toggle navigation</span>
					<span class="icon-bar"></span>
					<span class="icon-bar"></span>
					<span class="icon-bar"></span>
				</button>
				<a class="navbar-brand" href="#">Menu</a>
			</div>

			<!-- Collect the nav links, forms, and other content for toggling -->
			<div class="collapse navbar-collapse" id="bs-example-navbar-collapse-1">
			  <ul id="top_menu_tabs" class="nav navbar-nav">
				<li class="active"><a href="#">Link 1</a></li>
				<li><a href="#">Link 2</a></li>
				<li><a href="#">Link 3</a></li>
			 </ul>
			</div><!-- /.navbar-collapse -->
		</div><!-- /.container-fluid -->
	</nav>
</div>	  
```

### Step2. Add following javasciprt code

```JavaScript
  $(document).ready(function() {

	var responsiveNavTabs2Bar = function() {
		if ($(window).width() >= 768) {
			$('.responsive-nav-tabs2bar>nav.navbar').removeClass('navbar-default');
			$('.responsive-nav-tabs2bar>nav.navbar>.container-fluid>.navbar-header').hide();
			$('.responsive-nav-tabs2bar>nav.navbar>.container-fluid>.navbar-collapse>.nav').removeClass('navbar-nav').addClass('nav-tabs');
		}
		else {
			$('.responsive-nav-tabs2bar>nav.navbar').addClass('navbar-default');
			$('.responsive-nav-tabs2bar>nav.navbar>.container-fluid>.navbar-header').show();
			$('.responsive-nav-tabs2bar>nav.navbar>.container-fluid>.navbar-collapse>.nav').removeClass('nav-tabs').addClass('navbar-nav');
		}
	}
	
	var responsiveNavPills2Bar = function() {
		if ($(window).width() >= 768) {
			$('.responsive-nav-pills2bar>nav.navbar').removeClass('navbar-default');
			$('.responsive-nav-pills2bar>nav.navbar>.container-fluid>.navbar-header').hide();
			$('.responsive-nav-pills2bar>nav.navbar>.container-fluid>.navbar-collapse>.nav').removeClass('navbar-nav').addClass('nav-pills');
		}
		else {
			$('.responsive-nav-pills2bar>nav.navbar').addClass('navbar-default');
			$('.responsive-nav-pills2bar>nav.navbar>.container-fluid>.navbar-header').show();
			$('.responsive-nav-pills2bar>nav.navbar>.container-fluid>.navbar-collapse>.nav').removeClass('nav-pills').addClass('navbar-nav');
		}
	}
	
 	$(window).resize(function() {
		responsiveNavTabs2Bar();
		responsiveNavPills2Bar();
	});
	responsiveNavTabs2Bar();
	responsiveNavPills2Bar();
  });
```

### Step 3. Resize the browse and see it works!
