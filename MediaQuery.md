```
import 'package:flutter/material.dart';

void main() {
  runApp(MainApp());
}

class MainApp extends StatelessWidget {
  const MainApp({super.key});

  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      debugShowCheckedModeBanner: false,
      home: Scaffold(
        body: Column(
          mainAxisAlignment: MainAxisAlignment.center,
          children: [
            Container(
              height: MediaQuery.of(context).size.height * 0.3,
              width: MediaQuery.of(context).size.width * 0.8,
              color: Colors.blueGrey,
              child: Center(
                child: Text(
                  "Screen Size ${MediaQuery.of(context).size.width}",
                  style: TextStyle(fontSize: 28, color: Colors.white),
                ),
              ),
            ),
            SizedBox(height: 20),
            Row(
              spacing: 10,
              mainAxisAlignment: MainAxisAlignment.center,
              children: [
                Container(
                  height: MediaQuery.of(context).size.height * 0.1,
                  width: MediaQuery.of(context).size.width * 0.2,
                  color: Colors.blueGrey,
                ),
                Container(
                  height: MediaQuery.of(context).size.height * 0.1,
                  width: MediaQuery.of(context).size.width * 0.2,
                  color: const Color.fromARGB(255, 21, 226, 89),
                ),
                Container(
                  height: MediaQuery.of(context).size.height * 0.1,
                  width: MediaQuery.of(context).size.width * 0.2,
                  color: const Color.fromARGB(255, 198, 25, 204),
                ),
              ],
            ),
          ],
        ),
      ),
    );
  }
}

```


##  output:
<img height="300" alt="image" src="https://github.com/user-attachments/assets/251f3926-69b2-4e89-a34b-597c1f466963" />
<img  height="300" alt="image" src="https://github.com/user-attachments/assets/26f18d14-b924-4a9d-94f5-73d8b9828ae0" />



