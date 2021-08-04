# picture_verification_code example

```
void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      title: 'PictureVerificationCode Demo',
      theme: ThemeData(
        primarySwatch: Colors.blue,
      ),
      home: CodeTestPage(),
    );
  }
}

class CodeTestPage extends StatefulWidget {
  @override
  _CodeTestPageState createState() => _CodeTestPageState();
}

class _CodeTestPageState extends State<CodeTestPage> {
  @override
  Widget build(BuildContext context) {
    String code = "";
    for (var i = 0; i < 6; i++) {
      code = code + Random().nextInt(9).toString();
    }
    return Scaffold(
        appBar: AppBar(
          title: Text("图片验证码"),
        ),
        body: Container(
            alignment: Alignment.center,
            child: PictureVerificationCode(
              code: code, backgroundColor: Colors.white,
            )));
  }
}
```

![snapshot](https://github.com/waitwalker/Resources/blob/master/Flutter/picture_verification_code/example.png?raw=true)