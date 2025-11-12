## Code 

```
import 'package:flutter/material.dart';

void main() => runApp(MaterialApp(home: MyApp()));

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: const Text('AppBar'),
      ),
      body: const Center(
        child: Text(
          'Hello, Flutter!\nThis is Body',
          style: TextStyle(fontSize: 24),
        ),
      ),
      floatingActionButton: FloatingActionButton(
        onPressed: () {
            print('FAB Pressed!');
        },
        child: const Icon(Icons.home),
      ),
    );
  }
}

```

## Output:
<img height="300" alt="image" src="https://github.com/user-attachments/assets/4490d149-3dcd-4fc7-816c-ba4d4844b68a" />

