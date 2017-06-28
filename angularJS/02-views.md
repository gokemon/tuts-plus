AngularJS supports Single Page Application via multiple views on a single page.  AngularJS has provides ng-view and ng-template directives and $routeProvider services.

ng-view tag simply creates a place holder where a corresponding view (html or ng-template view) can be placed based on the configuration.
Define a div with ng-view within the main module.

    <div ng-app = "mainApp">
       <div ng-view></div>
    </div>    

ng-template directive is used to create an html view using script tag. It contains "id" attribute which is used by $routeProvider to map a view with a controller.

Define a script block with type as ng-template within the main module.

    <div ng-app = "mainApp">  
       <script type = "text/ng-template" id = "addStudent.htm">
      <h2> Add Student </h2>
      {{message}}
       </script>
    </div>    

$routeProvider is the key service which set the configuration of urls, map them with the corresponding html page or ng-template, and attach a controller with the same.

Define a script block with main module and set the routing configuration.

    var mainApp = angular.module("mainApp", ['ngRoute']);
    mainApp.config(['$routeProvider', function($routeProvider) {
       $routeProvider.   
       when('/addStudent', {
      templateUrl: 'addStudent.htm', controller: 'AddStudentController'
       }).   
       when('/viewStudents', {
      templateUrl: 'viewStudents.htm', controller: 'ViewStudentsController'
       }).   
       otherwise({
      redirectTo: '/addStudent'
       });
    }]);

Following are the important points to be considered in above example.
$routeProvider is defined as a function under config of mainApp module using key as '$routeProvider'.

$routeProvider.when defines a url "/addStudent" which then is mapped to "addStudent.htm". 
addStudent.htm should be present in the same path as main html page.If htm page is not defined then ng-template to be used with id="addStudent.htm". We've used ng-template.

"otherwise" is used to set the default view.

"controller" is used to set the corresponding controller for the view.