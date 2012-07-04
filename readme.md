# Countdown JS

This is a simple countdown script. I get too many clients asking for the same thing. I don't like the other scripts I saw online as they use a lot of inline Javascript and HTML. I wanted a script that is truly unobtrusive, and that you can re-use easily with any application. This is it. Enjoy!

Any bugs or issues, feel free to fork and do a pull request.

Contact:

	Leonard Teo
	leonard@ballistiq.com

# Usage

Include the countdown.js in your application in the <head> tags:
	
	<script src="countdown.js"></script>
	
Invoke the countdown like this:

	//You must always have the target date and the current date
	//The current date is the date of your server so that you don't run into timezone issues
	//Use your server side programming (PHP/Ruby/Python/ASP, etc) to output a date that you can read in using Javascript
	var target_date = new Date(2012, 12, 25, 0, 0, 0);
    var current_date = new Date(2012, 07, 04, 0, 0, 0);

	//Create the countdown object
	var count = new Countdown(target_date, current_date);
	
	//Run the countdown
	count.countdown(function(obj) {
		//Do anything you want with the obj, which contains days, hours, minutes, seconds
		//This will be called every one second as the countdown timer goes
		console.debug(obj);
		
		//E.g. you might use jQuery to update the countdown
		$('#days').html(obj.days);
		$('#hours').html(obj.hours);
		$('#minutes').html(obj.minutes);
		$('#seconds').html(obj.seconds);
	});
	

# License

    Copyright (C) 2012 Ballistiq Digital Inc.
    
    Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:
    
    The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.
    
    THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
