var app = angular.module('Prototipo', ['ui.bootstrap']);
app.controller('Control', function($scope, $http) {
      $http.get("http://localhost/SAD/php/select.php").then(
            function (res){
            $scope.names = res.data.datos;
            });
	$scope.buscar = function () {    
      	$scope.filtro=$scope.input;
   };
   
});

app.directive('ngEnter', function () {
    return function (scope, element, attrs) {
        element.bind("keydown keypress", function (event) {
            if(event.which === 13) {
                scope.$apply(function (){
                    scope.$eval(attrs.ngEnter);
                });
 
                event.preventDefault();
            }
        });
    };
});