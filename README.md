# FlutterProjects
All the Flutter Projects detailed out

## Lesson 1 - Flutter Basic App
App that says Hello world

Design Widget tree: https://app.diagrams.net/

![Basic App widget Tree](https://myoctocat.com/assets/images/base-octocat.svg)

Code: 
```
import 'package:flutter/material.dart';

void main() {
  runApp(
    const MaterialApp(
      // an app that uses material design (android)
      home: Center(
        child: Text(
          'Hello World',
        ),
      ),
    ),
  );
}

```

## Lesson 2 - I am Rich App
App that displays a diamond
