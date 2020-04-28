<!DOCTYPE html>
<head>
	<meta http-equiv="Content-Type" content="text/html; charset=utf-8" />
	<title></title>
	<meta name="description" content="" />
	<meta name="keywords"  content="" />
	<meta name="Resource-type" content="Document" />
	<link rel="stylesheet" type="text/css" href="assets/css/fullpage.css" />
	<link rel="stylesheet" type="text/css" href="assets/css/new.css" />
	<meta content="width=device-width, initial-scale=1" name="viewport" />
	<link href="https://fonts.googleapis.com/css?family=Open+Sans|Playfair+Display" rel="stylesheet">
</head>
<body>
	<div class="spinner-wrapper">
		<div class="spinner">
		  <div class="bounce1"></div>
		  <div class="bounce2"></div>
		  <div class="bounce3"></div>
		</div>
	</div>
	<nav>
		<a href="index.html"><span class="underline--magical"> Nicolas Dinh </span></a>
		<a href="/work.html"><span class="underline--magical"> Work </span></a>
		<a href="#3rdPage"><span class="underline--magical"> Contact Me </span></a>
	</nav>
<div id="fullpage">

	<div class="section " id="section0">

		<div class="intro">

			<div class="text-content">

				<h3><span><strong>Hello, I'm</strong></span><br>
					<span id="typed-strings">
						<span>Nicolas Dinh.</span>
						<span> a <span class="underline--magical"><a href="#secondPage/slide3">Web Designer,</a></span>
						a <span class="underline--magical"><a href="#secondPage/slide2">Social Media Coordinator</a></span>
						and I'm ready to work with <span class="underline--magical"><a href="#3rdPage">you.</a></span></span>
					</span>
					<span id="typed"></span>
				</h3>

			</div>
		</div>
		<p id="infoMenu">
			scroll for more
		</p>
	</div>

	<div class="section" id="section1">

	   <div class="slide" id="slide1" data-anchor="slide1">
			<div class="intro">
				<h1>Selected Works</h1>
			</div>
		</div>

	   <div class="slide" id="slide2" data-anchor="slide2">
			<h1><span class="underline--magical"><a href="/work.html#kingchildren">King Children</a></span></h1>
		</div>

		<div class="slide" id="slide3" data-anchor="slide3">
			<h1><span class="underline--magical"><a href="/work.html#pavlovagency">Pavlov Agency</a></span></h1>
		</div>

		<div class="slide" id="slide3" data-anchor="slide3">
			<h1><span class="underline--magical"><a href="/work.html#blackmarketusa">Black Market USA</a></span></h1>
		</div>

	</div>


	<div class="section" id="section2">

		<div class="intro">

			<button id='contact'><h1><span class="underline--magical">Want to work with me?</h1></span></button>

					<div id="contactForm">

				  <h2>Let's Work Together</h2>

					<form class="form" action="mailto:nicolas.h.dinh@gmail.com">
					    <div class="form-group">
					      <label class="form-label" for="first">Name</label>
					      <input id="first" class="form-input" type="text" />
					    </div>

					    <div class="form-group">
					      <label class="form-label" for="last">Email</label>
					      <input id="last" class="form-input" type="email" />
					    </div>

							<div class="form-group">
							 <label class="form-label" for="color">What do you need?</label>
							 <input id="color" class="form-input" type="text" />
						 </div>

							<span class="underline--magical"><button class="formBtn" type="submit">Send</button></span>

					  </form>
					</div>

		</div>

	</div>
</div>

</body>
<script type="text/javascript" src="js/type.js"></script>
<script type="text/javascript" src="typed/type.js"></script>
<script type="text/javascript" src="js/fullpage.js"></script>
<script type="text/javascript" src="js/underline.js"></script>
<script src='https://cdnjs.cloudflare.com/ajax/libs/babel-polyfill/6.26.0/polyfill.min.js'></script>
<script src='http://cdnjs.cloudflare.com/ajax/libs/jquery/2.1.3/jquery.min.js'></script>
<script>
$(document).ready(function() {
//Preloader
$(window).on("load", function() {
preloaderFadeOutTime = 500;
function hidePreloader() {
var preloader = $('.spinner-wrapper');
preloader.fadeOut(preloaderFadeOutTime);
}
hidePreloader();
});
});
</script>
<script type="text/javascript">
    var myFullpage = new fullpage('#fullpage', {
        anchors: ['firstPage', 'secondPage', '3rdPage'],
        sectionsColor: ['white', 'white', 'white'],
        slidesNavigation: true,
    });
</script>
<script>

$(function() {

	// contact form animations
	$('#contact').click(function() {
		$('#contactForm').fadeToggle();
	})
	$(document).mouseup(function (e) {
		var container = $("#contactForm");

		if (!container.is(e.target) // if the target of the click isn't the container...
				&& container.has(e.target).length === 0) // ... nor a descendant of the container
		{
				container.fadeOut();
		}
	});

});

$('input').focus(function(){
  $(this).parents('.form-group').addClass('focused');
});

$('input').blur(function(){
  var inputValue = $(this).val();
  if ( inputValue == "" ) {
    $(this).removeClass('filled');
    $(this).parents('.form-group').removeClass('focused');
  } else {
    $(this).addClass('filled');
  }
})
</script>
</html>
