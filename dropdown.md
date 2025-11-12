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
              'Hello, Flutter!\nYou have choosen:\nR:${((color?.r ?? 0) * 255).round()} G:${((color?.g ?? 0) * 255).round()}  B:${((color?.b ?? 0) * 255).round()}',
              style: TextStyle(
                fontSize: 24,
                color: Colors.white,
                fontWeight: FontWeight.bold,
              ),
              textAlign: TextAlign.center,
            ),
          ),
          const SizedBox(height: 20),
          DropdownMenu(
            inputDecorationTheme: const InputDecorationTheme(
              filled: true,
              fillColor: Colors.black54,
              border: OutlineInputBorder(
                borderRadius: BorderRadius.all(Radius.circular(12)),
                borderSide: BorderSide.none,
              ),
            ),
            textStyle: const TextStyle(
              fontSize: 20,
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
