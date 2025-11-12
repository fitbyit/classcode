## Practical 16: Use the Stack widget to overlay a Text widget on an Image
### Code
```dart
import 'package:flutter/material.dart';

void main() => runApp(MyApp());

class MyApp extends StatelessWidget {
  final List<Map<String, String>> imageData = [
    {
      'url': 'https://images.unsplash.com/photo-1507525428034-b723cf961d3e',
      'title': '1 Img'
    },
    {
      'url': 'https://images.unsplash.com/photo-1506744038136-46273834b3fb',
      'title': '2 Img'
    },
    {
      'url': 'https://images.unsplash.com/photo-1506744038136-46273834b3fb',
      'title': '3 Img'
    },
    {
      'url': 'https://images.unsplash.com/photo-1507525428034-b723cf961d3e',
      'title': '4 Img'
    },
    {
      'url': 'https://images.unsplash.com/photo-1506744038136-46273834b3fb',
      'title': '5 Img'
    },
  ];

  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      home: Scaffold(
        appBar: AppBar(
            title: Text('Images Stack'),
            backgroundColor: Colors.teal,
            foregroundColor: Colors.white,
        ),


        body: SingleChildScrollView(
          child: Column(
            children: imageData.map((item) => Padding(
              padding: const EdgeInsets.symmetric(vertical: 10),
              child: Center(
                child: Stack(
                  children: [
                    Container(
                      width: 400,
                      height: 250,
                      decoration: BoxDecoration(
                        borderRadius: BorderRadius.circular(25),
                        image: DecorationImage(
                          image: NetworkImage(item['url']!),
                          fit: BoxFit.cover,
                        ),
                        boxShadow: [
                          BoxShadow(
                              color: Colors.grey.withOpacity(0.4), 
                              blurRadius: 6, 
                              offset: Offset(3, 3))],
                      ),
                    ),
                    Container(
                      width: 400,
                      height: 250,
                      alignment: Alignment.bottomCenter,
                      padding: EdgeInsets.all(8),
                      decoration: BoxDecoration(
                        color: Colors.black54,
                        borderRadius: BorderRadius.circular(25),
                      ),
                      child: Text(
                        item['title']!,
                        style: TextStyle(
                            fontSize: 30, 
                            color: Colors.white, 
                            fontWeight: FontWeight.bold),
                      ),
                    ),
                  ],
                ),
              ),
            )).toList(),
          ),
        ),
      ),
    );
  }
}
```

## Output
<img  height="400" alt="image" src="https://github.com/user-attachments/assets/5b0c3e9b-f24a-4da1-ae4b-b9a022924b8e" />

