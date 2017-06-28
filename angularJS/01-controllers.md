AngularJS application mainly relies on ***Controllers to control the flow of data in the application***. A controller is defined using **ng-controller directive**. A *controller is a JavaScript object containing attributes/properties and functions*. Each controller accepts $scope as a parameter which refers to the application/module that controller is to control.

    <div ng-app = "" ng-controller = "studentController">
       ...
    </div>

Here we've declared a controller studentController using ng-controller directive. As a next step we'll define the studentController as follows −

    <script>
       function studentController($scope) {
      $scope.student = {
     firstName: "Mahesh",
     lastName: "Parashar",
     
     fullName: function() {
    var studentObject;
    studentObject = $scope.student;
    return studentObject.firstName + " " + studentObject.lastName;
     }
      };
       }
    </script>

studentController defined as a JavaScript object with $scope as argument.
$scope refers to application which is to use the studentController object.
$scope.student is property of studentController object.

firstName and lastName are two properties of $scope.student object. We've passed the default values to them.

fullName is the function of $scope.student object whose task is to return the combined name.

In fullName function we're getting the student object and then return the combined name.

As a note, we can also define the controller object in separate JS file and refer that file in the html page.

Now we can use studentController's student property using ng-model or using expressions as follows.

    Enter first name: <input type = "text" ng-model = "student.firstName"><br>
    Enter last name: <input type = "text" ng-model = "student.lastName"><br>
    <br>

You are entering: {{student.fullName()}}

We've bounded student.firstName and student.lastname to two input boxes.

We've bounded student.fullName() to HTML.

Now whenever you type anything in first name and last name input boxes, you can see the full name getting updated automatically.
