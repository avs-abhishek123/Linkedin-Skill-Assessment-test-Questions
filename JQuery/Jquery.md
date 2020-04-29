jQuery Assessment
-----------------
### This is only for informational purpose.
-----------------

First Header | Second Header
------------ | -------------
<br> <br><img src="https://github.com/avs-abhishek123/Linkedin-Skill-Assessment-test-Questions/blob/master/JQuery/JQueryImages/1.png" width="90%" height="50%"> )<br><br> | <br> <br><img src="https://github.com/avs-abhishek123/Linkedin-Skill-Assessment-test-Questions/blob/master/JQuery/JQueryImages/2.png" width="90%" height="50%"> )<br><br>
<img src="https://github.com/avs-abhishek123/Linkedin-Skill-Assessment-test-Questions/blob/master/JQuery/JQueryImages/3.png" width="90%" height="50%"> )<br><br>|<img src="https://github.com/avs-abhishek123/Linkedin-Skill-Assessment-test-Questions/blob/master/JQuery/JQueryImages/4.png" width="90%" height="50%"> )<br><br>
<img src="https://github.com/avs-abhishek123/Linkedin-Skill-Assessment-test-Questions/blob/master/JQuery/JQueryImages/5.png" width="90%" height="50%"> )<br><br>|<img src="https://github.com/avs-abhishek123/Linkedin-Skill-Assessment-test-Questions/blob/master/JQuery/JQueryImages/6.png" width="90%" height="50%"> )<br><br>
<img src="https://github.com/avs-abhishek123/Linkedin-Skill-Assessment-test-Questions/blob/master/JQuery/JQueryImages/7.png" width="90%" height="50%"> )<br><br>|<img src="https://github.com/avs-abhishek123/Linkedin-Skill-Assessment-test-Questions/blob/master/JQuery/JQueryImages/8.png" width="90%" height="50%"> )<br><br>
<img src="https://github.com/avs-abhishek123/Linkedin-Skill-Assessment-test-Questions/blob/master/JQuery/JQueryImages/9.png" width="90%" height="50%"> )<br><br>|<img src="https://github.com/avs-abhishek123/Linkedin-Skill-Assessment-test-Questions/blob/master/JQuery/JQueryImages/10.png" width="90%" height="50%"> )<br><br>
<img src="https://github.com/avs-abhishek123/Linkedin-Skill-Assessment-test-Questions/blob/master/JQuery/JQueryImages/11.png" width="90%" height="50%"> )<br><br>|<img src="https://github.com/avs-abhishek123/Linkedin-Skill-Assessment-test-Questions/blob/master/JQuery/JQueryImages/12.png" width="90%" height="50%"> )<br><br>
<img src="https://github.com/avs-abhishek123/Linkedin-Skill-Assessment-test-Questions/blob/master/JQuery/JQueryImages/13.png" width="90%" height="50%"> )<br><br>|<img src="https://github.com/avs-abhishek123/Linkedin-Skill-Assessment-test-Questions/blob/master/JQuery/JQueryImages/14.png" width="90%" height="50%"> )<br><br>

#### Q1. What's the difference between these two snippets?
`$('button').on('click', function(){
     alert('you clicked the button!');
 });
 $('button').click(function(){
     alert('you clicked the button!');
 });`

- Only the second one will work; jQuery does not have a function called .on. <<<<---Correct
- The second snippet will not function.
- Nothing - .click(function) is shorter way to write .on('click', function)
- The first snippet will execute for every button on the page, the second will only apply to the first button

#### Q2. What does the following line of code do?
`jQuery('p')`

- Loads a paragraph tag from a remote server using AJAX
- Aliases jQuery to a variable p
- Selects all paragraphs on the page <<<<---Correct
- Creates a new paragraph tag and inserts it into the body tag
 
#### Q3. Give the following HTML, how could we use one line to hide or show the button?
`<button class="btn btn-primary" type="submit">Continue to checkout</button>`

- $('.btn-primary').toggle(); ???? // toggle(true); & toggle(false);
- $('.btn-primary').showHide();
- $('.btn-primary').not(':visible').show();
- $('.btn-primary').css({ display: 'block'}); <<<<---Correct // ({ display: 'none'});

#### Q4. Working with AJAX, we may run into situations where a piece of code should not be run until after multiple AJAX,
#### calls have completed successfully. Say we need to call two external services for JSON data (a list of students, and 
#### a list of classes). And only after retrieving those data will we perform some manipulations on a page. What is the 
#### preferred way for dealing with this scenario?
#### https://example.com/json-api/students https://example.com/json-api/classes

- `$.get([
      'https://example.com/json-api/students',
      'https://example.com/json-api/classes'
   ], function(studentRequest, classRequest) {
      // the rest of the code goes here
});` <<<<<-CORRECT !

- `$.when(
      $.get('https://example.com/json-api/students'),
      $.get('https://example.com/json-api/classes')
   ).done(function(studentRequest, classRequest) {
      // the rest of the code goes here
});`

- `$.bind(
      $.get('https://example.com/json-api/students'),
      $.get('https://example.com/json-api/classes')
   ).done(function(studentRequest, classRequest) {
      // the rest of the code goes here
});`

- `$.ajax('https://example.com/json-api/students', {
   success: function(studentRequest) {
        $.ajax('https://example.com/json-api/classes', {
            success: function(classRequest) {
              // the rest of the code goes here
              }
        });
   }
});`   

#### Q5. Given the snippet of HTML below, what is the difference between the two lines that follow it?

<ul>
    <li>Item 1</li>
    <li>Item 2</li>
    <li>Item 3</li>
    <li>Item 4</li>
</ul>

===================

$('ul').find('li').get(2);
$('ul').find('li').eq(2);

- .get() retrieves a DOM element, and can't be chained, eq() retrieves a jQuery object, and can be chained.
- .get() retrieves a jQuery object, and can't be chained, eq() retrieves a DOM element, and can be chained.
- .get() retrieves a jQuery object, and is zero-indexed, eq() retrieves a DOM element, and is 1-indexed.
- .get() retrieves a DOM element, and is zero-indexed, eq() retrieves a jQuery object, and is 1-indexed.  <<<<--Correct !

#### Q6. Suppose we want to have an ball created from an HTML element (id=ball) move down and to the right
#### from its original location when clicked, and move back into its original place when finished. Given a starting
#### point of this, which of these snippets would accomplish that goal?

$('#ball').click(function() {
    // Our code goes here
});

- `$(this).animate({
    top: '+=100',
    left: '+=100',
}, {
    duration: 600,
    complete: function() {
        $(this).animate({
            top: '-=100',
            left: '-=100',
        }, 600)
    }
});`

- `$(this).animate({
    top: '-=100',
    left: '-=100',
}, 600, function() {
        $(this).animate({
            top: '+=100',
            left: '+=100',
        }, 600)
    }
});` <<<<----CORRECT !      

- `$(this).animate({
    top: '=100',
    left: '=100',
}, {
    duration: 600,
    complete: function() {
        $(this).animate({
            top: 0,
            left: 0,
        }, 600)
    }
});`

- `$(this).animate({
    top: '100',
    left: '100',
}, 600, function() {
        $(this).animate({
            top: 0,
            left: 0,
        }, 600)
    }
});`

#### Q7. Given the following CSS and HTML codes below, how could you apply the success class to the feedback div?

.success {
        color: green;
        background: #ddffdd;
}

<div class="feedback">
        Thank you for answering this survey.
</div>

- `$('.feedback').hasClass('.success');`
- `$.css('.feedback', '.success')`;
- `$('.feedback').addClass('.success');` <<<<---Correct ?
- `$('.feedback').css('.success');`

#### Q8. Below an example page snippet that includes a couple of messages in a list, and a code snippet that
#### retrieves a few hundred messages from a API endpoints using AJAX. How might we add these items to the 
#### page snippet in a way that avoids performance problems with DOM insertions?

<div class="message-area">
    <ul class="message-area--list">
        <li>Existing message 1</li>
        <li>Existing message 2</li>
    </ul>
</div>

$.get('//example.com/api/v1/message')
    .done(function(data) {
        var tonsOfItems = data.messages;
        // add all these messages to a large page
});

- `tonsOfItems.map(function(item) {
     $('.message-area--list').append('<li>'+item+'</li>');
});`

- `var tonsOfListItems = tonsOfItems.map(function(itme))  {
     return '<li>'+item+'</li>';
});
$('.message-area--list').append(tonsOfListItems.join(''));` 

- `Removing the event handlers with JavaScript will be slower than removing them 
$.each(tonsOfItems, function(idx, item) {
    $('<li>'+item+'</li>').appendTo($messageList);
});`
 
- `$.each(tonsOfItems, function(idx, item) {
    $('.message-area--list').append('<li>'+item+'</li>');
});`

#### Q9. What is jQuery?

- jQuery is a bridge between Java and Javascript that makes native apps easier to write.
- jQuery is a plugin for JavaScript that makes database queries easier to write.
- jQuery is a collection of JavaScript functions that makes finding and manipulating elements on a page, 
AJAX, and other things easier. <<<<---CORRECT !
- jQuery is a Chrome extension that allows users to create their own extensions with just a few lines of JavaScript.

#### Q10. We want to create a new jQuery plugin called linkUpdater that can be chained onto other jQuery
#### selector like a normal plugin. It should updates all the links in the referenced collection so they open 
#### in new windows or tabs. Below is the first cut. What is one problem with this plugin?

"user strict";
    $.linkUpdater = function() {
        this.find('a').attr('target', '_blank');
    }
) )( jQuery );

- this needs to be wrapped, like $(this), in order to be chained in a plugin. 
- jQuery plugins can't be safety authored in strict mode.
- In order to be used by other code, plugins need to be added to the global namespace, not wrapped in
function expression. <<<---CORRECT !
- Our plugin should extend jQuery.fn, not jQuery itself.

#### Q11. Generally speaking, when used on a web page, how should jQuery be installed, and why?

- Just before the closing body tag, because we want to avoid blocking other resources from loading, and 
we use the ready method to make sure our code fires after the DOM is ready <<<<---CORRECT!
- Using the highest version number possible because only jQuery 3 and up are compatible with Internet
Explorer 7

- In the head tag because we want jQuery available as soon as possible
- From a CDN because we want to be able to use jQuery online or offline

#### Q12. Given the following HTML, How could we make this button disappear from the page using jQuery?

<button> class="btn btn-primary" type="submit">Continue to checkout</button>

- $('.btn-primary').hide(); <<<---CORRECT
- $('.btn-primary:visible').not();
- $('.btn-primary').visibility(false);
- $('.btn-primary').show(false);

#### Q13. What is the difference between $('header').html() and $('header').text()?

- $('header').html() returns the inner HTML of the header. $('header').text() returns only the text <<<<--CORRECT
- $('header').html() returns only the HTML tags used, without the text. $('header').text() returns only the text
- $('header').html() strips all HTML from the header. $('header').text() always returns an empty string.
- $('header').html() returns all headers in an HTML document. $('header').text() the first line of a text file.

#### Q14. When writing jQuery plugins, we often provide default options that may be overridden by the end user.
#### What jQuery function is most useful for this purpose?

- $.extend <<<<---CORRECT
- $.clone
- $.fn.extend
- $.merge

#### Q15. There are times when you might want to programmatically trigger an event, instead of simply reacting to user 
#### input directly. Given this markup, Which choice will NOT cause a click event to the select box when 
#### the button is clicked?

<article>
    <div>
      Here's a button you can click: <button class="btn">Click Me</button>
    </div>   
    
    <form>
        <p>
            Further down the page, there's a select box.
        </p>
        <select>
            <option value="1">One</option>
            <option value="2">One</option>
            <option value="3">One</option>
            <option value="4">One</option>
        </select>
    </form>    
</article>

- `$('button').on('click.myApp', (function() {
        $('input[type=select]').trigger('click');
});` <<<<<----CORRECT !

- `$('button').on('click', (function() {
        $('input[type=select]').click());
});`

- `$('button').trigger(function() {
        $('input[type=select]').click();
});`

- `$('button').click(function() {
        $('input[type=select]').click();
});`
<br><br><br>
<img src="https://github.com/avs-abhishek123/Linkedin-Skill-Assessment-test-Questions/blob/master/JQuery/JQueryImages/15.png" width="80%" height="40%"> <br><br>
