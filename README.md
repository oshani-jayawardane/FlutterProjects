# FlutterProjects
All the Flutter Projects detailed out

Course: https://www.udemy.com/course/flutter-bootcamp-with-dart/ <br />
Course Resources: https://github.com/londonappbrewery/Flutter-Course-Resources <br />
Course Troubleshooting: https://github.com/DetainedDeveloper/App-Brewery-Flutter-Null-Safety <br />

### important links

Design Widget tree: https://app.diagrams.net/  <br /> 
Flutter Documentations - https://api.flutter.dev/flutter/material/material-library.html  <br /> 
Free icons: https://icons8.com/  <br /> 
Free vector images: https://www.vecteezy.com/  <br /> 
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


