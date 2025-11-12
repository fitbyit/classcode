## Practical 14: Implement a TextField widget to accept user input and display it using a Text widget.

### Code
```dart
import 'package:flutter/material.dart';

void main() => runApp(MaterialApp(home: UserInputApp()));

class UserInputApp extends StatefulWidget {
  @override
  _UserInputAppState createState() => _UserInputAppState();
}
class _UserInputAppState extends State<UserInputApp> {
  String _inputText = ''; // Stores the text entered by user
  
@override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(title: const Text('TextField Example')),
      body: Padding(
        padding: const EdgeInsets.all(16.0),
        child: Column(
          children: [
            TextField(
              onChanged: (value) {
                setState(() {
                  _inputText = value; // Update text as user types
                });
              },
              decoration: const InputDecoration(
                border: OutlineInputBorder(),
                labelText: 'Enter your text',
              ),
            ),
            const SizedBox(height: 20),
            Text('You typed: $_inputText', style: const TextStyle(fontSize: 20),
            ),
          ],
        ),
      ),
    );
  }
}
```
### Output:

<img height="400" alt="image" src="https://github.com/user-attachments/assets/acd96125-9e5a-4f99-9df9-17a455f80fff" />

