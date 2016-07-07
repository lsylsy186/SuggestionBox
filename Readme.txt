This website designed by using AngularJS, html, css, javascript, which needs to be run in a Apache HTTP server.

User Stories:
What are user stories: User stories are descriptions from the perspective of the end-user meant to capture the essence of a program's features. In the case of your game, the end-user is whoever is playing your game. User stories are usually in the first-person, or in other words, "I" statements.

As a user: 
* I want to be able to create a suggestion.
* I want to be able to upvote a suggestion.
* I want the most upvoted suggestions to rise to the top.
* I want to comment on a suggestion.

Starting from scratch: 
* What kinds of problems does a real suggestion box solve?
* How can a suggestion box app help alleviate those problems?
* Does a suggestion box app cause any problems that a real suggestion box doesn't?

Translate Ideas into code:
* A view for the whole list of suggestions.
* A way to input suggestions.
* A way to upvote suggestions.
* A way to comment on a suggestion.

Outline:
* Suggestion List:
	- A home.html file for the view.
	- A home controller for suggestion item actions.
* Comments:
	- A post.html file for the view, so we can see an individual post to comment on.
	- A posts controller for comments actions.
* Store Suggestions and Comments:
	- A service for storing data.

Adding Some Style:
* add Bootstrap: <link href="http://maxcdn.bootstrapcdn.com/bootstrap/3.3.2/
css/bootstrap.min.css" rel="stylesheet">

Throwing More Suggestions Into The Hat:
*****************************************************************
<form ng-submit="addSuggestion()" style="margin-top: 50px">
<h3> Submit Your Suggestion </h3>
<div class="form-group">
<input type="text" class="form-control" placeholder="Great ideas here" ng-model="title"></input>
</div>
<button type="submit" class="btn btn-primary">Suggest</button>
</form>
*******************************************************************

To add comments, I will need to:
 1. Add a new view, to show a single suggestion with the comments below it.
	* This will involve adding routes to my app.
 2. Add comments to the suggestions.js service.
 3. Create a controller for comments, to let users add a new comment.

    Also, since we are adding another view and another controller, it's smart to start organizing our view code using the MVC paradigm. Once we add routes, we can give our views their own files, and we can route to them based on the URL.

Adding Routes:
 1. Insert in the angular-route.min.js into index.html.
	<link src="https://code.angularjs.org/1.2.28/angular-route.min.js" type="text/javascript">
 2. In app.js, add ngRoute as a parameter.
	
