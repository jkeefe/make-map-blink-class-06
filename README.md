#Make Map Blink 6: Javascript & Charts

To get all of the files for this lesson, use the "Download Zip button over there --->"

###FILES USED: 
Everything in the folder "live demo" (included in this repo).

##First, a little html

- Open the file `index.html` with a text editor. The simpler the better. 
- If it's TextEdit, be sure to use "plain text" mode: Format --> Make Plain Text.
- Better to use TextWrangler (free) or TextMate (not free, but what I use) or Sublime Text (what many use, not free)

It's blank! Let's change that.

- For the first line, declare it an html file with this: `<!DOCTYPE html>`
- Almost all html commands have an open tag and a close tag, like `<strong>` (open) and `</strong>` (close)
- Type in the open and close tags for "html":

	<html>
	</html>
	
OK, now we need two more sections *between* those two tags: head and body:

	<html>
	
	<head>
	</head>
	
	<body>
	</body>
	
	</html>
	
Now, let's just test this out. Put 'Hello, world!' between the body tags.

	<body>
	Hello, world!
	</body>
	
Drag the whole index.html into a browser window.

Cool.

##Take a peek at Highcharts

Highcharts is a great little JavaScript library, which is basically a program that someone else wrote so that you don't have to. you can do lots with it, but we'll do some simple things.

Head over to the [Highcharts website](http://highcharts.com).

- Click Demo -> Highcharts Demos
- Browse all of the different kinds of charts you can make

This is where we download the highcharts library. I've already included it for you in the "live demo" folder. It's in a subfolder called 'js' for JavaScript. Let's tell our html document to use it, and another library there called jQuery.

Between the `<head>` tags, put:
	
	<script src="js/jquery-1.6.4.min.js" type="text/javascript"></script>
	<script src="js/highcharts.js" type="text/javascript"></script>
	
Type that carefully!

Then do one more thing: Add a pair of `<script>` tags in the head. Leave a little space between them to make things easier:
	
	<script>
	
	</script>
	
This is where we're going to put the chart code!

Go back to the Highcharts website.

- Click Demo -> Highcharts Demos
- Choose "basic line" if it's not chosen already
- Click "view options"

This is the JavaScript code that generated the line chart. Copy and paste all the code in that window.

Don't worry if you don't understand what's there. We'll explore it together.

One last thing ... we need to tell Highcharts where to put the chart. The "container" if you will. It should go in a "div" in the `<body>` of the html. Like this this:
	
	<body>
		<div id="container"></div>
	</body>
	
Save that and drag it over to your browser!

OK ... Now we're going to make this a school attendance chart, [like this one](http://project.wnyc.org/jan-school-attendance/). 

Here's the data we need:

	Date, Attendance
	'Th 1/2', 73.93
	'Fri 1/3', 0
	'Mon 1/6', 89.69
	'Tue 1/7', 72.59
	'Wed 1/8', 89.15
	'Th 1/9', 91.41
	'Fri 1/10', 89.91
	'Mon 1/13', 91.3
	'Tue 1/14', 91.34
	'Wed 1/15', 91.67
	'Th 1/16', 91.74
	'Fri 1/17', 90.58
	'Tue 1/21', 89.22
	'Wed 1/22', 47.1

And we use [Mr. Data Converter](http://shancarter.github.io/mr-data-converter/) to turn it into the kinds of data Highcharts uses. (Try the JSON - "Column Arrays" option.)

	name: 'Attendance',
	data: [73.93, 0,  89.69,  72.59,  89.15,  91.41,  89.91,  91.3, 91.34,  91.67,  91.74,  90.58,  89.22, 47.1]

	categories: [
	'Th 1/2', 'Fri 1/3', 'Mon 1/6', 'Tue 1/7', 'Wed 1/8', 'Th 1/9', 'Fri 1/10', 'Mon 1/13', 'Tue 1/14', 'Wed 1/15', 'Th 1/16', 'Fri 1/17', 'Tue 1/21','Wed 1/22'
	]
	
Put those where they seem to go in the code.

Fix the other titles. 

What else can you do?

If you wanted to embed it, you could put it in the cloud and use this:

  <iframe frameborder="0" height="650" scrolling="no" src="URL_GOES_HERE" width="100%"></iframe>





