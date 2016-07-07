app.controller('suggestionController', ['$scope', '$routeParams',
 'suggestions', function($scope, $routeParams, suggestions) {

    $scope.post = suggestions.posts[$routeParams.id];
    $scope.addComment = function(){
        if(!$scope.my_comments || $scope.my_comments === '' ){
            return;
        }
        $scope.post.comments.push({
            body:$scope.my_comments,
            upvotes:0,
        });
        $scope.my_comments = '';
    };
    $scope.remove = function($index){
        $scope.post.comments.splice($index, 1);
    };
    $scope.upvoteComments = function(comment){
        comment.upvotes += 1;
    };

 }])