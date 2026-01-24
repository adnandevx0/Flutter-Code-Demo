# Flutter-Code-Demo

<h3>Class 1: Basic Text , Icon</h3>

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


<h3> Class 2: Text, Icon, Image, Container, Listview </h3>


<pre>

  
import 'package:flutter/material.dart';

void main(){
  runApp(Myapp());
}

class Myapp extends StatelessWidget{
  Widget build(BuildContext context){
    return MaterialApp(
      debugShowCheckedModeBanner: false,
        home:  Scaffold(
          backgroundColor: Colors.greenAccent,
          appBar: AppBar(backgroundColor: Colors.green,title: Text("Adnan Devf", style:
          TextStyle(color: Colors.cyan, backgroundColor: Colors.amber,fontWeight: FontWeight.bold ),
          )
            ,),
          body: Center(
            child: ListView(

              children: [
                Container(
                  width: 200,
                  color: Colors.blueGrey,
                  alignment: Alignment(22, 22),
                  child: Text("lsdfhsfdf  dsfdsfdsf lsdfhsfdf  dsfdsfdsf sdfsdfdsfdsf dsffdsfdslsdfhsfdf  dsfdsfdsf sdfsdfdsfdsf dsffdsfdslsdfhsfdf  dsfdsfdsf sdfsdfdsfdsf dsffdsfdslsdfhsfdf  dsfdsfdsf sdfsdfdsfdsf dsffdsfds sdfsdfdsfdsf dsffdsfds",
                    textAlign: TextAlign.start,
                    maxLines: 2,
                    textDirection:
                    TextDirection.ltr, style: TextStyle(
                        color: Colors.black),),
                ),
                //Icons
                Container(
                  color: Colors.yellow,
                  child:  Icon(Icons.android, color: Colors.green, size: 50,) ,
                ),
                Container(
                  color: Colors.blue,
                  child:  Image.network("https://www.facebook.com/images/icons/FBLogo_Blueprint.png",
                    height: 22, width: 60, ) ,
                ),
                Container(
                  color: Colors.redAccent,
                  child:  Image.asset("333.jpg",
                    height: 511, width: 111, fit: BoxFit.fill, ) ,
                )
              ],
            ) ,

          ),

        ),
    );
  }
}
  
</pre>
