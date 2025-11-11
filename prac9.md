```
import 'package:flutter/material.dart';

void main() {
  runApp( MaterialApp(home: HomePage(),));
}

class HomePage extends StatefulWidget {
  @override
  State<HomePage> createState() => _MyAppState();
}

class _MyAppState extends State<HomePage>{
  final txtcon = TextEditingController();
  String? name;
@override
Widget build(BuildContext context){
  return Scaffold(
    appBar: AppBar(
      title: Text("Pracical9"),
    ),
    body: Column(
      mainAxisAlignment: MainAxisAlignment.center,
      children: [
        TextField(
          controller: txtcon,
          decoration : InputDecoration(
            hintText: "Enter Text",
          ) 
        ),
        ElevatedButton(
          onPressed: () => setState(()=> name= txtcon.text),
          child: Text("Submit"),
        ),
        Text("You have entered: $name"),
      ],
    ),
  );
}
}

```
