app.controller('HomeController', ['$scope', 'suggestions',
 function($scope, suggestions) {

    $scope.posts = suggestions.posts;

    $scope.addSuggestion = function(){
        //if input empty, don't submit
        if(!$scope.title || $scope.title === ''){
            return;
        }

        //push suggestion posts in suggestions.js
        suggestions.posts.push({
            title: $scope.title,
            upvotes: 0,
            comments:[],
        });

        //after submit, clear input
        $scope.title = '';
    };
    $scope.remove = function($index){
        $scope.posts.splice($index, 1);
    };
    $scope.upVote = function(post){
        post.upvotes += 1;
    };
}]);