# b24_widgets

**b24_widgets** is a Flutter Package that include existing sample widget such as TextInput, PhoneInput,DateInput,TimeInput and other widgets ..etc

## Widgets
- **ExTextInput**
- **ExSelectTool**
- **ExDatePicker**
- **ExCheckBox**

## Getting started
To use the **b24_widgets** package in your Flutter project, follow these steps:

### Add the dependency
Add the following dependency to your `pubspec.yaml` file:
```yaml
dependencies:
  b24_widgets: ^0.0.19
```
### Usage

**ExTextInput Type Passwords** 

```ymal
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
    externalValidator: (value) {
      if (value != controlPass.text) {
      return 'Your passowrd not match!';
    }},),
```

**ExTextInput Type Email** 

```yaml
     ExTextInput(
      label: 'Email',
      hintText: 'Enter Email',
      type: ExInputType.email,
      sizeLabel: ExInputSizeType.small,
      prefixIcon: Icon(Icons.email_rounded),
      onTap: () {},
      ),
```
**ExTextInput Type Text** 

``` yaml
     ExTextInput(
      label: 'Text',
      hintText: 'Enter your content',
      isRequired: false,
      type: ExInputType.text,
      sizeLabel: ExInputSizeType.small,
      inputFormatters: [FilteringTextInputFormatter.singleLineFormatter],
      textCapitalization: TextCapitalization.words,
      maxLines: 10,
      ),
```

**ExDatePicker** 

``` yaml
     ExDatePicker(
      labelText: 'Date Picker',
      weekDayfull: true,
      dialogCalendarPickerValue: _dialogCalendarPickerValue, // Defualt date picker range
      selectColor: Colors.amber,
      sizeLabel: ExInputSizeType.medium,
      currenYearColor: Colors.red,
     ),
```

**ExCheckBox** 

```yaml
     ExCheckBox(
      checkBoxSizes: CheckBoxSize.small,
      onTapCheck: () {},
      onTapUncheck: () {},
      activeColor: Colors.green,
      ),
```

**ExSelectionTool** 

```yaml
   ExSelectionTool(
     allItems: myItem.countries,
     isMultiSelect: true,
     prefixIcon: const Icon(Icons.search),
     suffixIcon: const Icon(Icons.arrow_drop_down_rounded),
     sizeLabel: ExInputSizeType.medium,
     textColor: Colors.red,
     radiusSize: 10.0,
    ),
```


**Example Full Usage**

``` yaml 
import 'package:b24_widgets/widgets/others/ex_date_picker.dart';
Widget build(BuildContext context) {
    // Show defualt range date picker
    final List<DateTime?> _dialogCalendarPickerValue = [
    DateTime.now(),
    DateTime.now().add(const Duration(days: 3)),
    ];

    return Scaffold(
      appBar: AppBar(
        backgroundColor: Theme.of(context).colorScheme.inversePrimary,
        title: Text(widget.title),
      ),
      body: Center(
        child: Column(
          mainAxisAlignment: MainAxisAlignment.center,
          children: <Widget>[
            ExDatePicker(
             labelText: 'Date Picker',
             weekDayfull: true,
             dialogCalendarPickerValue: _dialogCalendarPickerValue,
             selectColor: Colors.amber,
             sizeLabel: ExInputSizeType.medium,
             currenYearColor: Colors.red,
                ),
          ],
        ),
      ),
      floatingActionButton: FloatingActionButton(
        onPressed: _incrementCounter,
        tooltip: 'Increment',
        child: const Icon(Icons.add),
      ), 
    );
  }
  ``````
