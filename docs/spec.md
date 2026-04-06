BAIS:3300 – Digital Product Management
Page 1 of 6
Creating a website with Flask
Purpose
The purpose of this assignment is to practice building your first dynamic website using a Python web
framework called Flask.
You will create a small flask app using the code quality pipeline tools.

Create web pages using Jinja templating language
12) Edit app.py to render a template.
BAIS:3300 – Digital Product Management
Page 2 of 6
13) Add render template to your Flask import
from flask import Flask, render_template
BAIS:3300 – Digital Product Management
Page 3 of 6
14) Edit your home route function so it doesn’t return “Hello world!!” but instead returns a web page.
return render_template('index.html')
15) Create static and templates folders.
a) In static, create a CSS subfolder.
b) In CSS, create a stylesheet.css file.
c) In stylesheet.css set the background color to your favorite color.
16) In templates, create a base.html template file.
17) In base.html, use Emmett to create a starter HTML 5 file.
18) Inside <title> element, add {% block title %} {% endblock%}
19) Add a link to your custom css file inside the <head> element.
<link rel="stylesheet" type="text/css"
href="{{ url_for('static', filename='css/stylesheet.css') }}" />
20) Inside <body> element, add {% block body %} {% endblock %}
21) In templates, create index.html file.
22) Add {% extends 'base.html' %} as the first line so this file knows when it loads it must first load
the template file base.html.
23) Next, add {% block title %} Welcome to my page {% endblock%} so this text is passed into
the <title> element on base.html.
24) Add page body content
{% block body %}
<main>
<h1>Mike Colbert</h1>
<p>
Lorem ipsum dolor sit amet consectetur adipisicing elit. Sit minus, iste ea cumque et
placeat non vero, veritatis quis quia minima, quod fuga! Sequi necessitatibus at ab aliquid
voluptatem illo.
</p>
</main>
{% endblock %}
25) Save all your file changes.
BAIS:3300 – Digital Product Management
Page 4 of 6
26) Run your Flask application with python app.py
27) View your page in your browser.
a) Does your home page appear?
b) Do you see your name and the paragraph of lorem ipsum?
c) Is your background color the color you wanted?
d) Is the page title set correctly?
28) Take a screenshot of your browser running your basic web page.
29) Commit and push your changes.
Style your page with Bootstrap 5.3
30) In base.html, in the <head> element, remove the link to your existing stylesheet.css.
31) In the <head> element, add a link to Bootstrap CSS delivered from the Bootstrap content delivery
network. This code can be found on the ICON assignment.
32) Between the body’s {% endblock %} and the </body> element, add a link to the two JavaScript files
needed to Bootstrap from the Bootstrap content delivery network. This code can be found on the
ICON assignment.
33) In index.html, give the <main> element a class of container.
34) View your page in your browser.
35) Take a screenshot of your browser running your Bootstrap styled home page.
36) Commit and push your code.
Create a second web page
37) Create a second page named about.html. You could probably just copy, rename, and edit
index.html.
a) If you do, remember to change the page title.
b) Content for the about.html page goes between the open and close <main> element.
c) If you want, copy some of the content from your homework in module 8 and paste it here. Edit
as necessary.
38) Edit app.py to add a second route (“/about”) with a new function named about_page that renders
the template about.html.
39) Take a screenshot of your browser running your Bootstrap styled about page.
BAIS:3300 – Digital Product Management
Page 5 of 6
BAIS:3300 – Digital Product Management
Page 6 of 6
Create a menu
40) In base.html, paste the menu code - found on the ICON assignment - between <body> and {% block
body %}.
41) Edit the menu to remove the search functionality and the drop-down menu. You can also remove
brand. Edit the remaining two pages to point to your index.html and about.html.
42) View your web page in your browser.
a) Is your menu visible?
b) Does it work? Can you use it to visit both pages?
c) When you shrink the width of the web browser, does it change to the “hamburger” menu?
43) Take a screenshot of your browser running your web page showing the full width menu.
44) Take a screenshot of your browser running your web page with the “hamburger” menu.
Deliverables
• Please PDF your Word document of screenshots. It makes grading MUCH easier.
• Upload the PDF of your screenshot document to the ICON Assignment
• Provide a link to the URL for the GitHub repository for this assignment.
