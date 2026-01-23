# Flutter-Code-Demo

<h3>Class 1</h3>

<pre>
import 'package:flutter/material.dart';
import 'package:google_fonts/google_fonts.dart';

void main(){
  runApp(Myhome());
}

class Myhome extends StatelessWidget {
  Widget build(BuildContext context){
    return MaterialApp(
      home: Scaffold(

        appBar: AppBar(title: Text("Hello Flutter", style: GoogleFonts.robotoMono(backgroundColor: Colors.deepPurple, color: Colors.amberAccent,), ), backgroundColor: Colors.amberAccent,),
        body: Row(
          mainAxisAlignment: MainAxisAlignment.end,
          children: [

            Text("Adsad", style: TextStyle(color: Colors.red),),
            Row(
              children: [
                Container(
                  child: Text("Adnasnds"),
                  height: 22,
                  width: 22,
                  color: Colors.cyanAccent,
                ),
              ],
            )
          ],
        ),
          floatingActionButton: FloatingActionButton(onPressed: () {},
          child: Icon(Icons.add_a_photo),
    ),
      ),
      );
  }
}
</pre>
