# textfield
flutte
////text field
import 'package:flutter/material.dart';
import 'package:flutter/rendering.dart';

void main() => runApp(MyApp());

class MyApp extends StatefulWidget {
  @override
  
  _MyAppState createState() => _MyAppState();
}

class _MyAppState extends State<MyApp> {
  TextEditingController controller = TextEditingController();
  
  @override

  Widget build(BuildContext context) {
    return MaterialApp(
      home: Scaffold(
        appBar: AppBar(
          title: Text("STMIK INDONESIA PADANG "),
          
        ),
        body: Container(
          margin: EdgeInsets.all(15),
          child: Column(
            mainAxisAlignment: MainAxisAlignment.spaceAround,
            children: <Widget>[
              TextField(
                decoration: InputDecoration(
                 ///fillColor: Colors.blueGrey,
                ///filled: true,
                  ////icon:Icon(Icons.account_box),
                  ///prefixText: 'NoBp',
                  prefixIcon: Icon(Icons.account_circle),
                  
                  ///prefixStyle: TextStyle(color: Colors.black,fontWeight: FontWeight.w400),
                   labelText: "NOMOR BP",
                    hintText: "Nomor BPNYA",
                  border: OutlineInputBorder(borderRadius: BorderRadius.circular(20))
                ),
                maxLength: 10,
                onChanged: (value) {
                  setState(() {});
                },
                controller: controller,
              ),
              Text(controller.text)
            ],
          ),
        ),
      ),
    );
  }
}

