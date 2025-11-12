## Change Background Color dynamic using DropdownMenu

### Code
```dart
import 'package:flutter/material.dart';

void main() => runApp(MaterialApp(home: MyApp()));

class MyApp extends StatefulWidget {
  @override
  State<MyApp> createState() => _MyAppState();
}

class _MyAppState extends State<MyApp> {
  MaterialColor? color;
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      backgroundColor: color ?? Colors.grey[500],
      appBar: AppBar(title: const Text('AppBar')),
      body: Column(
        mainAxisAlignment: MainAxisAlignment.center,
        children: [
          Center(
            child: Text(
              'Hello, Colors!',
              style: TextStyle(
                fontSize: 24,
                color: Colors.white,
                fontWeight: FontWeight.bold,
              ),
              textAlign: TextAlign.center,
            ),
          ),
          const SizedBox(height: 5),
          DropdownMenu(
            hintText: 'Select a color',
            inputDecorationTheme: const InputDecorationTheme(
              filled: true,
              hintStyle: TextStyle(
                fontSize: 18,
                color: Colors.white70,
                fontWeight: FontWeight.bold,
              ),
              fillColor: Colors.black54,
              border: OutlineInputBorder(
                borderRadius: BorderRadius.all(Radius.circular(12)),
                borderSide: BorderSide.none,
              ),
            ),
            textStyle: const TextStyle(
              fontSize: 18,
              color: Colors.white,
              fontWeight: FontWeight.bold,
            ),
            width: MediaQuery.of(context).size.width * 0.6,
            onSelected: (value) {
              setState(() {
                color = value;
              });
            },
            dropdownMenuEntries: const [
              DropdownMenuEntry(value: Colors.deepPurple, label: 'Deep Purple'),
              DropdownMenuEntry(value: Colors.red, label: 'Red'),
              DropdownMenuEntry(value: Colors.blue, label: 'Blue'),
            ],
          ),
        ],
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

## Output
<img  height="400" alt="image" src="https://github.com/user-attachments/assets/ccf83a69-4704-4f97-9b2b-c2478b9437b3" />

