# FlutterProjects
All the Flutter Projects detailed out

Course: https://www.udemy.com/course/flutter-bootcamp-with-dart/ <br />
Course Resources: https://github.com/londonappbrewery/Flutter-Course-Resources <br />
Course Troubleshooting: https://github.com/DetainedDeveloper/App-Brewery-Flutter-Null-Safety <br />

### important links

Design Widget tree: https://app.diagrams.net/  <br /> 
Flutter Documentations - https://api.flutter.dev/flutter/material/material-library.html  <br /> 

Flutter Theme data - https://api.flutter.dev/flutter/material/ThemeData-class.html <br />
Flutter cookbook - https://docs.flutter.dev/cookbook <br />

Material Design for Flutter: https://material.io/components?platform=flutter <br />
Material color palette and icons: https://www.materialpalette.com/ <br />
Flutter Design icons class: https://api.flutter.dev/flutter/material/Icons-class.html <br />

App icon generator: https://appicon.co/ <br /> 
Free icons: https://icons8.com/  <br /> 
Free vector images: https://www.vecteezy.com/  <br /> 

Free sounds: https://freesound.org/ <br /> 

Flutter layout cheat sheet: https://medium.com/flutter-community/flutter-layout-cheat-sheet-5363348d037e <br /> 

### useful shortcuts
alt + enter -> instant wrappers etc
ctrl + Q -> Quick docs

### adding own images to Flutter

add a new directory – images <br />
edit **pubspec.yaml** file – assets <br />
recorrect indentation - indent 2 spaces !!!important <br />
pub get <br />
<br />
**YAML** is a data serialization language that is often used for writing configuration files. <br />
<br />
**Image.asset('images/dice1.png'),** <br /><br />
// above is a much more convenient way to specify asset images - (refer documentation) than, <br />
**Image(** <br />
  **image: AssetImage('images/dice1.png'),** <br />
 **),** <br />

### changing icon image

convert image using: appicon.co <br /><br />

1. For **Android** – app – src – main – res – replace the mipmap files <br />
2. For **iOS** – runner – replace the assets.xcassets <br />

### changing icon shape

1. right click project – flutter – open android module – new window <br />
2. android module – app - res – right click –  new – image asset – pick path to wanted icon image – resize – finish <br />

### Running App on physical device

1. For **Android** - settings – about phone – build number – tap tap tap – enter developer mode – go to developer options – enable usb debugging <br />

## Hot reload
  doesn't change the state of the app (ex: input data)

## Hot Restart
  changes the state of the app and restarts 

### enabling hot reload
we need to have a stateless widget
  1. type "stless" for short
  2. enter (creates a boilerplate)
  3. give the class a name
  4. copy matreialApp inside the stateless widget's return statement 
  5. in runApp() in main -> type the name of the class you gave

## Lesson 1 - Flutter Basic App
App that says Hello world

## Lesson 2 - I am Rich App
App that displays a diamond

## Lesson 3 - MiCard (Personal Business Card App)
### Cloning a repository: <br />
  1. Copy github URL <br />
  2. In Android studio - File -> New -> Project from version control -> Git -> Copy URL <br />
  3. Select directory -> clone <br />
  4. red lines on main.dart -> pubspec.yaml -> get dependencies <br />

### containers
containers are single-child layout widgets (refer documentation) <br />
container takes the size of the child content <br />
to wrap container in safe area of the phone -> alt + enter -> wrap in widget -> safeArea <br />

inspect -> flutter inspector <br /><br />

different ways of setting margins <br />
  1. margin: EdgeInsets.all(50.0),
  2. margin: EdgeInsets.symmetric(vertical: 50.0, horizontal: 20.0),
  3. margin: EdgeInsets.fromLTRB(10.0, 20.0, 30.0, 40.0),
  4. margin: const EdgeInsets.only(left: 30),

Same with paddings <br />

## Lesson 4 - Dicee App

Functions - creating and calling functions <br />
() { // something }; is an anonymous function <br />
<br />
Stateless widget -> responds to no state change <br />
Stateful widget -> responds to state changes <br />
<br />
**important** -> define variables outside the widget build -> not subjected to hot reload always <br />
Expanded class -> fills the width or height of the device depending on the orientation <br />
TextButton -> onpressed() {\\ do something - better to write in a function} <br />
|_ child -> whatever text / image to be pressed <br />

## Lesson 5 - Xylophone App

Flutter packages - https://pub.dev/packages?q=sdk%3Aflutter <br />
install and import packages and access them <br />

## Lesson 6 - Quizzler App

//TODO: something <br />
Lists - like arrays <br />
List<dataType> ListName = [item1, item2, item3]; <br />
Classes in dart -> lib -> right click -> new dart file -> "filename.dart" <br /><br />
**The Four Pillars of Object-Oriented Programming** <br />
1. Abstraction <br />
2. Encapsulation. <br />
3. Inheritance. <br />
4. Polymorphism. <br />
 
```
void main() {

 Car myNormalCar = Car();
 print(myNormalCar.numberOfSeats);
 myNormalCar.drive();
 
 // inheritance
 ElectricCar myTesla = ElectricCar();
 myTesla.drive();
 myTesla.recharge();
 
 // polymorphism
 LevitatingCar myMagLev = LevitatingCar();
 myMagLev.drive();
  
 SelfDrivingCar myWaymo = SelfDrivingCar('1 Hacker Way');
 myWaymo.drive();

}
 
class Car {
 
 int numberOfSeats = 5;
 
 void drive(){
  print('wheels turn');
 }

}
 
class ElectricCar extends Car {

 int batteryLevel = 100;
 
 void recharge() {
  batteryLevel = 100;
 }
 
}
 
class LevitatingCar extends Car {

 @override
 void drive() {
  print('glide forward');
 }
}

class SelfDrivingCar extends Car {
  
  String destination = '';
  
  // constructor
  SelfDrivingCar(String userSetDestination) {
    destination = userSetDestination;
  }
  
  // when we need to inherit the method from parent (super class) but also need to add to it
  @override
  void drive() {
    super.drive();
    print('sterring towards $destination');
  }
}
```
 
**Dart Constructors**

 ```
 void main() {
  
  Human jenny = Human(height: 15, weight: 3.5);
  print(jenny.height);
  
  Human james = Human(height: 20, weight: 4.2);
  print(james.height);
  
}

class Human {
  
  double height = 0;
  double weight = 0;
  
//   Human({double height = 0, double weight = 0}) {
//     this.height = height;
//     this.weight = weight;
//   }
  
//   if we say height = height dart will get confused
  
  Human({this.height = 0, this.weight = 0});
  
}
 ```

 ## Lesson 7 - BMI calc
 
 making classes with repetitive code instantly - flutter outline -> widget -> right click -> extract widget -> rename <br />
 when to use keys - https://www.youtube.com/watch?v=kn0EOS-ZiIc <br />
 <br />
 **const vs final** <br />
const - can't change anywhere else or change be changed in run time either.  <br />
 final - can be changed in run time. ex: DateTime.now() can't be assigned to const but can be assigned to final <br />

 ** ENUMS **
  ```
 void main(){
  
  Car myCar = Car(carStyle: CarType.SUV);
  print(myCar);
  
  
}

class Car {
  
  CarType carStyle;
  
  Car({this.carStyle = CarType.sedan});
  
}

enum CarType{
    sedan,
    conertible,
    SUV,
    hatchback,
    coupe,
  }
 ```
 
 **FUNCTIONS AS FIRST ORDER OBJECTS**
 
 ```
 void main(){
  
  Car myCar = Car(drive: slowDrive);
  print(myCar.drive);
  myCar.drive();
  
  myCar.drive = fastDrive;
  print(myCar.drive);
  myCar.drive();
  
  
}

class Car {
  
  Car({required this.drive});
  
  Function drive;
}
  
  void slowDrive(){
    print('Driving slowly.');
  }
  
  void fastDrive(){
    print('Driving super fast.');
  }
 ```
