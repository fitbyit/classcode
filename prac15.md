## Design a Flutter app with a Container widget and customize its padding, margin, and color.
### Code
```dart
import 'package:flutter/material.dart';

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      title: 'Container Example',
      home: Scaffold(
        appBar: AppBar(
          title: Text('Container'),
          backgroundColor: Colors.teal,
          foregroundColor: Colors.white,
        ),

        body: Center(
          child: Container(
            // Margin: Space outside the container
            margin: EdgeInsets.all(20.0),
            
// Padding: Space inside the container
            padding: EdgeInsets.symmetric(horizontal: 30.0, vertical: 20.0),
            
//Background Color, Rounded corners and shadow
            decoration: BoxDecoration(
              color: Colors.lightBlueAccent,
              borderRadius: BorderRadius.circular(12),
              boxShadow: [
                BoxShadow(
                  color: Colors.grey.withOpacity(0.5),
                  blurRadius: 6,
                  offset: Offset(3, 3),
                ),
              ],
            ),
            child: Text(
              'Hello, Flutter!',
              style: TextStyle(
                fontSize: 24,
                color: Colors.white,
                fontWeight: FontWeight.bold,
              ),
            ),
          ),
        ),
      ),
    );
  }
}
```

## Output

<img height="400" alt="image" src="https://github.com/user-attachments/assets/4df52542-3934-422d-9aa3-a0b5b3fe9cda" />

