# Splash Screen
### File 1: main.dart
This is the entry point of your Flutter application. It should define the MyApp widget, which sets up the application's theme and initial route.
```
import 'package:flutter/material.dart';
import 'splash_screen.dart'; // Import the SplashScreen widget

void main() => runApp(MyApp());

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      title: 'Flutter Demo',
      theme: ThemeData(
        primarySwatch: Colors.blue,
      ),
      home: SplashScreen(), // Use SplashScreen as the initial route
    );
  }
}
```
