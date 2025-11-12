```
import 'package:flutter/material.dart';

void main() => runApp(MaterialApp(home: MyApp()));

class MyApp extends StatelessWidget {
  MyApp({super.key});
  final List<Map<String, dynamic>> boxes = [
    {'color': Colors.red, 'text': 'Red'},
    {'color': Colors.green, 'text': 'Green'},
    {'color': Colors.blue, 'text': 'Blue'},
    {'color': Colors.orange, 'text': 'Orange'},
    {'color': Colors.purple, 'text': 'Purple'},
  ];

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(title: const Text('Scrollable Colored Boxes in Row')),
      body: SingleChildScrollView(
        scrollDirection: Axis.horizontal, // horizontal scrolling
        child: Row(
          crossAxisAlignment: CrossAxisAlignment.end,
          children: boxes.map((box) {
            return Container(
              height: 200,
              width: 200,
              decoration: BoxDecoration(
                color: box['color'],
                borderRadius: BorderRadius.circular(10),
              ),
              alignment: Alignment.center,
              margin: const EdgeInsets.all(5),
              child: ElevatedButton(onPressed: () {}, child: Text(box['text'])),
            );
          }).toList(),
        ),
      ),
    );
  }
}

```
