## Square of a Number using StatefullWidget

```dart
import 'package:flutter/material.dart';

void main() => runApp(MaterialApp(home: MyApp()));

class MyApp extends StatefulWidget {
  @override
  State<MyApp> createState() => _MyAppState();
}

class _MyAppState extends State<MyApp> {
  TextEditingController nub1 = TextEditingController();
  num? result;

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      backgroundColor: Colors.deepPurple[200],
      appBar: AppBar(title: const Text('AppBar')),
      body: Column(
        mainAxisAlignment: MainAxisAlignment.center,
        children: [
          Padding(
            padding: const EdgeInsets.all(8.0),
            child: TextField(
              style: const TextStyle(fontSize: 20, color: Colors.white),
              controller: nub1,
              decoration: const InputDecoration(
                border: OutlineInputBorder(),
                fillColor: Colors.black54,
                filled: true,
                hintText: 'Enter Number',
                hintStyle: TextStyle(color: Colors.white),
              ),
            ),
          ),
          const SizedBox(height: 10),
          ElevatedButton(
            onPressed: () {
              setState(() {
                final input = num.tryParse(nub1.text);
                if (input != null) {
                  result = input * input;
                } else {
                  result = null;
                }
              });
            },
            child: const Text('Calculate Square'),
          ),
          const SizedBox(height: 10),
          Container(
            padding: const EdgeInsets.all(20),
            child: Text(
              result == null
                  ? 'Enter a valid number'
                  : 'The square is: $result',
              style: const TextStyle(fontSize: 24, color: Colors.white),
            ),
          ),
        ],
      ),
    );
  }
}
```

## Output

<img height="400" alt="image" src="https://github.com/user-attachments/assets/88e1cdbd-0552-4705-9f66-f9612b77c027" />
