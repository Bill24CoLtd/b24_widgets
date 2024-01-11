# b24_widgets

**b24_widgets** is a Flutter Package that include existing sample widget such as TextInput, PhoneInput,DateInput,TimeInput and other widgets ..etc

## Widgets
- **ExTextInput**
- **ExPhoneInput**
- **ExTimeInput**
- **ExDateInput**

## Getting started
To use the **b24_widgets** package in your Flutter project, follow these steps:

### Add the dependency
Add the following dependency to your `pubspec.yaml` file:
```yaml
dependencies:
  b24_widgets: ^0.0.1
```
### Usage
import 'package:b24_widgets/widgets/inputs/ex_text_input.dart';


``` yaml 
Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        backgroundColor: Theme.of(context).colorScheme.inversePrimary,
        title: Text(widget.title),
      ),
      body: Center(
        child: Column(
          mainAxisAlignment: MainAxisAlignment.center,
          children: <Widget>[
             ExTextInput(
              inputType: ExInputType.password,
              prefixIcon: Icon(
                Icons.lock,
                color: Theme.of(context).dividerColor.withOpacity(.7),
              ),
              label: S.current.password,
              isRequired: true,
              controller: context
                  .read<LoginPageProvider>()
                  .txtPasswordLoginController,
              onSubmitted: (_) =>
                  pro.submitButtonCont.requestInvokeOnPress!(),
            ),
          ],
        ),
      ),
      floatingActionButton: FloatingActionButton(
        onPressed: _incrementCounter,
        tooltip: 'Increment',
        child: const Icon(Icons.add),
      ), // This trailing comma makes auto-formatting nicer for build methods.
    );
  }
