import 'package:flutter/material.dart';
import 'package:flutter/src/widgets/basic.dart';
import 'package:flutter/src/widgets/basic.dart';
import 'package:flutter/src/widgets/framework.dart';
import 'package:flutter/src/widgets/framework.dart';

void main() {
  runApp(MyApp() //also we will run our statless class MyApp here as a router

      );
}

//using stless to create a stateless widget boiler plate and
//return our MaterialApp within the stateless widget

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      home: Scaffold(
        backgroundColor: Colors.teal,
        body: SafeArea(
          //An example of fucking nested columns and rows

          child: Container(
            //Main container
            child: Row(
              //Main row container
              crossAxisAlignment:
                  CrossAxisAlignment.stretch, //to strech across column
              mainAxisAlignment:
                  MainAxisAlignment.spaceBetween, //to space between both row

              children: <Widget>[
                //children of row spaced out
                Container(
                  //1st container
                  color: Colors.red,
                  width: 100,
                ),
                Container(
                  //child container or nested container inside container to have children
                  child: Column(
                    //main column
                    mainAxisAlignment:
                        MainAxisAlignment.center, //to space between both row
                    children: <Widget>[
                      Container(
                        //1st box in column in row
                        color: Colors.yellow,
                        width: 100,
                        height: 100,
                      ),
                      Container(
                        //2nd box in column in row
                        color: Colors.green,
                        width: 100,
                        height: 100,
                      ),
                    ],
                  ),
                ),
                Container(
                  //finally the 3rd row of streched box
                  color: Colors.blue,
                  width: 100,
                ),
              ],
            ),
          ),
        ),
      ),
    );
  }
}
