# b24_widgets

**b24_widgets** is a Flutter Package that include existing sample widget such as TextInput, PhoneInput,DateInput,TimeInput and other widgets ..etc

## Widgets
- **ExTextInput**
- **ExPhoneInput**
- **ExTimeInput**
- **ExDateInput**
- **ExSelectTool**
- **ExDatePicker**

## Getting started
To use the **b24_widgets** package in your Flutter project, follow these steps:

### Add the dependency
Add the following dependency to your `pubspec.yaml` file:
```yaml
dependencies:
  b24_widgets: ^0.0.12
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
            ExSelectionTool(
                  allItems: myItem.countries,
                  isMultiSelect: true,
                  prefixIcon: const Icon(Icons.search),
                  suffixIcon: const Icon(Icons.arrow_drop_down_rounded),

                ),
                  ExTextInput(
                    type: ExInputType.passwords,
                    confirmPassword: false,
                    controller: controlPass,
                    isShowRuleValidate: true,
                    label: 'Password',
                  ),
                  ExTextInput(
                    type: ExInputType.passwords,
                    confirmPassword: true,
                    label: 'Confirm Password',
                    controller: controlConfirm,
                    controllerConfirm: controlPass,
                    // externalValidator: (p0) {
                    //   if (p0 != controlPass.text) {
                    //     return 'not match';
                    //   }
                    //   return null;
                    // },
                  ),
                ExDatePicker(
                  weekDayfull: true,
                ),],
        ),
      ),
      floatingActionButton: FloatingActionButton(
        onPressed: _incrementCounter,
        tooltip: 'Increment',
        child: const Icon(Icons.add),
      ), // This trailing comma makes auto-formatting nicer for build methods.
    );}
  
  ``````
