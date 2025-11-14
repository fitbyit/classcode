### Stack

```
import 'package:flutter/material.dart';

void main() {
  runApp(const MyApp());
}

class MyApp extends StatelessWidget {
  const MyApp({super.key});

  // This widget is the root of your application.
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      title: 'Flutter App!!',
      home: Stack(
        children: [
          Container(
            width: 300,
            height: 300,
            color: Colors.deepPurple[500],
          ),
          Container(
            width: 200,
            height: 200,
            color: Colors.deepPurple[300],
          ),
          Container(
            width: 100,
            height: 100,
            color: Colors.deepPurple[100],
          )
        ],
      )
    );
  }
}
```
