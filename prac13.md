## Practical 13: Create a simple counter app using StatefulWidget to increment and display a number.

### Code
```dart
import 'package:flutter/material.dart';

void main() => runApp(MaterialApp(home: CounterApp()));

class CounterApp extends StatefulWidget {
  @override
  _CounterAppState createState() => _CounterAppState();
}

class _CounterAppState extends State<CounterApp> {
  int _counter = 0;

  void _incrementCounter() {
    setState(() {
      _counter++;
    });
  }

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(title: const Text('Counter App')),
      body: Center(
        child: Column(
          mainAxisAlignment: MainAxisAlignment.center,
          children: [
            Text(
              '$_counter',
              style: const TextStyle(fontSize: 50, fontWeight: FontWeight.bold),
            ),
            const SizedBox(height: 20),
            ElevatedButton(
              onPressed: _incrementCounter,
              child: const Text('Counter++'),
            ),
            ElevatedButton(
              onPressed: () {
                setState(() {
                  _counter = 0;
                });
              },
              child: const Text("Reset"),
            ),
          ],
        ),
      ),
    );
  }
}

```

## Output

<img height="400" alt="image" src="https://github.com/user-attachments/assets/cc232a1d-f16b-43a2-ba79-29302d401751" />



    `
