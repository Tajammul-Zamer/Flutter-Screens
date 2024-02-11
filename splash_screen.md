# Splash Screen
<img src="/Assets/Screenshot_1707670389.png" src="/Assets/Screenshot_1707670395.png" width="500" height="500" alt="Alt text" title="a title">
<img src="/Assets/Screenshot_1707670395.png" width="500" height="500" alt="Alt text" title="a title">

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
### File 2: splash_screen.dart
This file defines the SplashScreen widget, which is displayed when the app is launched. After a delay, it navigates to the HomeScreen.
```
import 'package:flutter/material.dart';
import 'dart:async';
import 'home_screen.dart'; // Import the HomeScreen widget

class SplashScreen extends StatefulWidget {
  @override
  _SplashScreenState createState() => _SplashScreenState();
}

class _SplashScreenState extends State<SplashScreen> {
  @override
  void initState() {
    super.initState();
    Timer(Duration(seconds: 3), () {
      Navigator.of(context).pushReplacement(MaterialPageRoute(builder: (_) => HomeScreen()));
    });
  }

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      body: Center(
        child: Text('Splash Screen', style: TextStyle(fontSize: 24, fontWeight: FontWeight.bold)),
      ),
    );
  }
}
```
### File 3: home_screen.dart
This file contains the HomeScreen widget, which is the main content of your app displayed after the splash screen.
```
import 'package:flutter/material.dart';

class HomeScreen extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: Text('Home Screen'),
      ),
      body: Center(
        child: Text('Welcome!', style: TextStyle(fontSize: 24)),
      ),
    );
  }
}
```
<img src="/Assets/Screenshot_1707670389.png" width="100" height="100" alt="Alt text" title="a title">
<img src="/Assets/Screenshot_1707670395.png" width="100" height="100" alt="Alt text" title="a title">

