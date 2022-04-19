-Frontend development framework from google.Flutter is Googl's free and open-source UI framework for creating native mobile applications.
-A 'tool' that allows you to build native cross-platform (iOS, Android) apps with one programming langeuage and codebase
-Flutter is not a programming language.it's a software deelopment kit(SDK) with prewritten code, consisting of ready-to-use and customizable widgets,as well as libraries,tools and documentation that together serve to build cross-platform apps.
-SDK - tools to compile your code to native machine code + develope with ease.
-Framework/Widget library - Re-usable UI building blocks (= Widgets)
-Dart is a programming language developed by Google - Object-oriented & strongly typed.
focused on frontend (mobile apps,web) user interface(UI) development

Flutter --> Dart framework, providing utility Functions & UI elements(Widgets)
Framework --> Set of features

In Flutter everything is Widget, Widget is just a code snippet, an instruction you placed in your code.
Your apps UI is a Widget tree.

Flutter simply compile that dart code to native code for these different platforms,and that happens with the help of Flutter SDK.

Alternative to Flutter is react native, Flutter doesn't use Platform Primitives.

Flutter doesn't compile your code to some native equivalent or native alternatives, instead Flutter ships with it's own engine which controls the entire screen.Flutter controls every pixel which is drawn. :Greater control, less platform-limitations, no 'translation loss'.

Material Design - Material is a Design system created by Google.it's not Google's style for everyone! it is indeed highly customizable (and works on iOS devices too). Material design is built into Flutter but you also find App-styled (Cupertion) widgets.

Widget - is a class and every class automatically also is a type.Which is provided by material dart. every widget is just dart class which in the end has a build method.
Every Widget in flutter needs to extend StatelessWidget or StatefulWidget and each of these classes will force you to add a build method because in the end flutter will always call that build method for you.We dont call it ,Flutter calls it

we dont have separate styling language, we style widgets through the arguments. and if a certain widget doesn't take a certain argument,then you have to use another widget and wrap the widget which you want to style with it.