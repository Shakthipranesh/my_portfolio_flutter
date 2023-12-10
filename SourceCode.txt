import 'package:flutter/material.dart';

void main() {
  runApp(
    MaterialApp(
      home: ID_Card(),
    ),
  );
}

class ID_Card extends StatefulWidget {
  const ID_Card({super.key});

  @override
  State<ID_Card> createState() => _ID_CardState();
}

class _ID_CardState extends State<ID_Card> {

  int studentlevel = 2;

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: Text("MY ID_CARD",
          style: TextStyle(
            color: Colors.black,
            fontWeight: FontWeight.bold,
          ),
        ),
        elevation: 0.0,
        centerTitle: true,
        backgroundColor: Colors.green.shade300,
      ),
      floatingActionButton: FloatingActionButton(
        onPressed: (){
          setState(() {
            studentlevel += 1;
          });
        },
        child: Icon(Icons.add),
        backgroundColor: Colors.green.shade300,
      ),
      body: Padding(
        padding: EdgeInsets.fromLTRB(30.0, 40.0, 30.0, 0.0),
        child: Column(
          crossAxisAlignment: CrossAxisAlignment.start,
          children: [
            Center(
              child: CircleAvatar(
                backgroundImage: AssetImage("assets/my_photo.jpg"),
                radius: 50.0,
              ),
            ),
            Divider(
              height: 40.0,
              color: Colors.grey.shade400,
            ),
            Text(
              "NAME:",
              style: TextStyle(
                color: Colors.grey[900],
                letterSpacing: 2.0,
                fontSize: 18.0,
                fontWeight: FontWeight.bold,
              ),
            ),
            SizedBox(height: 5.0,),
            Text(
              "SHAKTHI PRANESH L",
              style: TextStyle(
                color: Colors.grey[900],
                letterSpacing: 2.0,
                fontSize: 28.0,
                fontWeight: FontWeight.bold,
              ),
            ),
            SizedBox(height: 15.0,),
            Text(
              "ROLE:",
              style: TextStyle(
                color: Colors.grey[900],
                letterSpacing: 2.0,
                fontSize: 18.0,
                fontWeight: FontWeight.bold,
              ),
            ),
            SizedBox(height: 5.0,),
            Text(
              "INTERN",
              style: TextStyle(
                color: Colors.grey[900],
                letterSpacing: 2.0,
                fontSize: 28.0,
                fontWeight: FontWeight.bold,
              ),
            ),
            SizedBox(height: 20.0,),
            Row(
              children: [
                Icon(
                  Icons.email,
                  color: Colors.grey.shade900,
                ),
                SizedBox(width: 4.0,),
                Text(
                  "shakthipranesh20@gmail.com",
                  style: TextStyle(
                    color: Colors.grey.shade900,
                    fontSize: 22.0,
                    fontWeight: FontWeight.w500,
                  ),
                ),

              ],
            ),
            SizedBox(height: 15.0,),
            Text(
              "FLUTTER DEVELOPMENT LEVEL:",
              style: TextStyle(
                color: Colors.grey[900],
                letterSpacing: 2.0,
                fontSize: 18.0,
                fontWeight: FontWeight.bold,
              ),
            ),
            SizedBox(height: 5.0,),
            Text(
              "$studentlevel",
              style: TextStyle(
                color: Colors.grey[900],
                letterSpacing: 2.0,
                fontSize: 28.0,
                fontWeight: FontWeight.bold,
              ),
            ),


          ],
        ),
      ),

      backgroundColor: Colors.green.shade100,
    );
  }
}
