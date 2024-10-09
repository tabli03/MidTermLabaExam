# MidTermLabaExam

import 'package:flutter/material.dart';

class Counter extends StatelessWidget {
  const Counter({super.key});

void CallBack(){
  print('The Button was Pressed');
}
// Updated parent widget.
  @override
  Widget build(BuildContext context) {
    return Row(
      mainAxisAlignment: MainAxisAlignment.center,
      children: <Widget>[
        ElevatedButton(
          onPressed: CallBack,
          child: const Text('Button'),
        ),
        const SizedBox(width: 16),
        Text('Count:'),
      ],
    );
  }
}
void main() {
  runApp(
    const MaterialApp(
      home: Scaffold(
        body: Center(
          child: Counter(),
        ),
      ),
    ),
  );
}

// From stateful widget, converted into stateless widget.
// Removed the _counter variable, functions, and the set state method.
/* dito gumamit ako ng CallBack function para ma call yung ipiprint na message 
   output na ilalagay kapag kiniclick yung button lalabas yung output the "button was pressed"
   kase ito ay isang StatelessWidget
*/
