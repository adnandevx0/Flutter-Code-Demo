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


<h3> Class 3: actions, leading, TextButton, IconButton,  </h3>

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
          appBar: AppBar( leading:
          // Image.asset("333.jpg"),

            Icon(Icons.home),
            backgroundColor: Colors.green,title: Text("Adnan Devf", style:
          TextStyle(color: Colors.cyan, backgroundColor: Colors.amber,fontWeight: FontWeight.bold ),),
          actions: [
            //Pop up Notefications
            Builder(builder:
            (context){
              return IconButton(onPressed: () {
                ScaffoldMessenger.of(context).showSnackBar(SnackBar(content:Text("Admanasd",style: TextStyle(color: Colors.red),)
                  ,duration: Duration(seconds: 1), backgroundColor: Colors.blue,)
                );
              }, icon: Icon(Icons.add_a_photo_rounded));
            }
            ),
          ],
          ),
          body: Center(
            child: Column(
              mainAxisAlignment: MainAxisAlignment.start,
              children: [
                Container(
                  width: 200,
                  color: Colors.blueGrey,
                  alignment: Alignment.center,
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
                    height: 112, width: 160, ) ,
                ),
                Container(
                  color: Colors.redAccent,
                  child:  Image.asset("333.jpg",
                    height: 221, width: 221, fit: BoxFit.fill, ) ,
                ),
                Container(
                  color: Colors.yellow,
                  height: 22, width: 222,
                  child:
                  Builder(builder:
                  (context){
                    return TextButton(onPressed: () {
                      ScaffoldMessenger.of(context).showSnackBar(SnackBar(content: Text("Adnasnd")));
                    } , child: Text("Click Me and Show Noti", style: TextStyle(color: Colors.blue),));
                  }
                  )
                  ,

                ),
              ],
            ) ,

          ),

        ),
    );
  }
}
  
</pre>

<h3> Class 4: খেয়াল কর এখানে আমরা MaterialApp রিটার্ন নেইনি আমরা অন্য ফাংশন থেকে রিটার্ন দিয়েছি কেবল Scaffold তাহলে কাজ করব, showDialog  </h3>

<pre>
import 'package:flutter/material.dart';

void  main(){
  runApp(MyApp());
}

class MyApp extends StatelessWidget{
  Widget build(BuildContext context){
    return MaterialApp(
      debugShowCheckedModeBanner: false,
      // আদনান খেয়াল কর এখানে আমরা MaterialApp রিটার্ন নেইনি আমরা অন্য ফাংশন থেকে রিটার্ন দিয়েছি কেবল Scaffold তাহলে কাজ করবে
      home: AppMAin() ,
    );
  }
}


class AppMAin extends StatelessWidget{
  Widget build(BuildContext context){
    return Scaffold(
        appBar: AppBar(
          backgroundColor: Colors.pinkAccent,
          title: Text("Tom App"),
          leading: Icon(Icons.add),
          actions: [
            Builder(builder: (context){
              return IconButton(onPressed: () {
                ScaffoldMessenger.of(context).showSnackBar(SnackBar(
                  backgroundColor:Colors.indigoAccent,content:
                Text("adnan",style:
                TextStyle(color: Colors.cyanAccent),)
                  ,duration: Duration(seconds: 1),));
              } , icon: Icon(Icons.camera_alt));
            })
          ],
        ),
        body: Column(
          children: [
            Container(
              alignment: Alignment.topLeft,
              height: 200,
              width: double.infinity, // infinity দেওয়া হয়েছে সব ফোনের স্ক্রিনে ফিট হওয়ার জন্য।,
              color: Colors.amber,
              child:Row(
                children: [
                  Text("Hi I am Tom",style: TextStyle(
                    color: Colors.pink,
                    fontSize: 30,
                  ),),
                   // see showDialog 
                  TextButton(style: TextButton.styleFrom(
                      backgroundColor: Colors.indigoAccent,
                      foregroundColor: Colors.lightGreen
                  ),onPressed: () {
                    showDialog(context: context, builder:
                        (context){
                      return AlertDialog(
                        title: Text("asd"),
                        content: Text("sad"),
                      );
                    }
                    );
                  } , child:
                  Text("Click Me",style: TextStyle(fontSize: 20,color: Colors.cyanAccent),),
                  ),
                ],
              ),
            )
          ],
        ) ,
      );
  }
}
</pre>


<h3> Class 5: ElevatedButton, </h3>

<h4> ElevatedButton, shape( Radius ), side( border ),GestureDetector,Icon Button,Text Button,  </h4>
<pre>
  Container(
                width: 100,
                color: Colors.amber,
                child: ElevatedButton( style: ElevatedButton.styleFrom(
                  backgroundColor: Colors.deepOrangeAccent,
                  foregroundColor: Colors.amberAccent,
                  shape:ContinuousRectangleBorder(
                      borderRadius: BorderRadiusGeometry.circular(9)
                  ) ,
                  side: BorderSide(
                      color: Colors.black87,
                    width: 3
                  ) ,

                ), onPressed: () {
                  print("Press");
                } , child: Text("Press")),
              ),
</pre>

<h4> GestureDetector,Icon Button,Text Button, </h4>
<pre>

            //Text Button
            Container(
              height:70,
              width:double.infinity ,
              color: Colors.teal,
              child: 
              TextButton( style:TextButton.styleFrom(
               backgroundColor: Colors.deepOrange,
                textStyle: TextStyle(color: Colors.amberAccent, fontSize: 30)
              ),
                  onPressed: () {} , child:
              Text("Chick me")
              ),
            ),

            
            //Icon Button
            Container(
              height:70,
              width:double.infinity ,
              color: Colors.teal,
              child:
              IconButton( style: IconButton.styleFrom(
                foregroundColor: Colors.amber,
                backgroundColor: Colors.blue,
              ) ,
                  onPressed: () {} ,
                  icon: Icon(Icons.all_inclusive_outlined,size: 40,))
              ,
              ),
        
  
  //GestureDetector
            Container(
              height:70,
              width:double.infinity ,
              color: Colors.teal,
              child: GestureDetector(
                onTap: () {
                  print("One Tap");
                },
                  onLongPressUp: () {
                  print("Long press");
                  },
                onDoubleTap: () {
                  print("Two Tap");
                },
                child:
                Text("G",style: TextStyle(backgroundColor: Colors.amber),)
              ) ,
            ),
</pre>
<h4> InkWell  </h4>
<pre>
   Container(
              height: 100,
              width: double.infinity,
              //এখানে যদি কালার ব্যবহার করি তাহলে বাটনে ক্লিক করার সময় যে কালার ওইগুলো শো করবে না
              //color: Colors.blue,
              child: InkWell(
                  splashColor: Colors.amberAccent,
                  radius: 200,
                  borderRadius: BorderRadius.circular(30),
                  onTap: () {
                    print("One Tap");
                  },
                  onLongPressUp: () {
                    print("Long press");
                  },
                  onDoubleTap: () {
                    print("Two Tap");
                  },
                  child:
                  Text("Click me",style: TextStyle(fontSize: 44),)
              ) ,
            )
</pre>
<h4> TextField  </h4>
<pre>
  TextField(
              maxLength: 3,
              style: TextStyle(
                color: Colors.blue,
                fontSize: 20,
              ),
              decoration:InputDecoration(
                hintText: "Enter Your Name",
                hintStyle: TextStyle(
                  color: Colors.amber,
                ),
                //label: Text("Email"),
                labelText: "asd",
                border: OutlineInputBorder(
                  borderRadius: BorderRadius.circular(4),
                ),
                focusedBorder:
                OutlineInputBorder(
                  borderSide: BorderSide(
                    color: Colors.black87,
                    width: 3
                  )
                ),
                //defult
                enabledBorder:
                OutlineInputBorder(
                  borderSide: BorderSide(color: Colors.deepOrange)
                ),
                disabledBorder:
                OutlineInputBorder(borderSide:
                  BorderSide(color: Colors.greenAccent),

                ),
                //background color
                fillColor: Colors.pink,
                filled: true,
                //before inpoted text
                //way 1
                prefix: Column(
                  children: [
                    Icon(Icons.thirty_fps_rounded)
                  ],
                ),
                //way 2 :
               // prefixIcon: Icon(Icons.thirty_fps_rounded) ,

                //end inpoted text
                suffixIcon: Icon(Icons.fax_rounded,color: Colors.green,) ,
              ),

            )
</pre>


<h4> TextFromField,   </h4>
<pre>
 Container(
              height: 50,
              width: double.infinity,
              // color: Colors.teal,
              child:
              Padding(padding: EdgeInsetsGeometry.all(4),child:
              TextFormField(
               // maxLength: 2,
                style: TextStyle(
                  color: Colors.blue,
                  fontSize: 20,
                ),
                decoration:InputDecoration(
                  hintText: "Enter Your Name",
                  hintStyle: TextStyle(
                    color: Colors.amber,
                  ),
                  //label: Text("Email"),
                  labelText: "asd",
                  border: OutlineInputBorder(
                    borderRadius: BorderRadius.circular(4),
                  ),
                  focusedBorder:
                  OutlineInputBorder(
                      borderSide: BorderSide(
                          color: Colors.black87,
                          width: 3
                      )
                  ),
                  //defult
                  enabledBorder:
                  OutlineInputBorder(
                      borderSide: BorderSide(color: Colors.deepOrange)
                  ),
                  disabledBorder:
                  OutlineInputBorder(borderSide:
                  BorderSide(color: Colors.greenAccent),
                  ),
                 //background color
                  fillColor: Colors.pink,
                  filled: true,
                ),
               //data validatios
               // validator: ;
              )
              ,),
            ),
</pre>


<h4> Container,   </h4>

<pre>

   Container(
              height: 300,
              width: 300,
              decoration: BoxDecoration(
                color: Colors.yellow,
                //borderRadius: BorderRadius.circular(40),
                //border: Border.all(color: Colors.red,width: 22)

                  //remove borderRadius: BorderRadius.circular(40),
                border: Border(
                  top:BorderSide(color: Colors.green,width: 10),
                  bottom: BorderSide(color: Colors.black, width: 15)
                ),
                //background image
                image:  DecorationImage(image:
                    AssetImage('assets/333.jpg'),
                  fit: BoxFit.cover
                ),
                //shadow
                boxShadow: [
                  BoxShadow(
                    color: Colors.pink,
                  spreadRadius: 2,
                    blurRadius: 2,
                    offset:Offset(0,3)
                  )
                ]
              ),

              alignment: Alignment.center,
              child: Text("AD",style: TextStyle(
                color: Colors.white,
                fontSize: 100,
                fontWeight: FontWeight.bold,
              ),),
            ),
  
</pre>

<h4> ListView  </h4>

<pre>

  ListView(
              //vertical, horizontal
              scrollDirection: Axis.vertical,
              children: [
                Text("Adnan Devf", style: TextStyle(color: Colors.pink, fontSize: 50),),
                Text("Adnan Devf", style: TextStyle(color: Colors.pink, fontSize: 50),),
                Text("Adnan Devf", style: TextStyle(color: Colors.pink, fontSize: 50),),
                Text("Adnan Devf", style: TextStyle(color: Colors.pink, fontSize: 50),),

              ],



   ListView.builder(
          itemCount: 20,
          itemBuilder: (context, index) {
        return Container(
          height: 50,
          width: double.infinity,
          color: index % 2 == 0 ? Colors.green : Colors.redAccent,
          child: Text("$index", style: TextStyle(
            color: Colors.white,
            fontSize: 30,
            fontWeight: FontWeight.bold,
          ),),
        );
      }) 
</pre>
