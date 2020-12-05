# country_state_city_picker

A flutter package for showing a country, states, and cities. In addition it gives the possibility to select a list of countries, States and Cities depends on Selected.

<div style="text-align:center">
<img src="https://github.com/prof22/country_state_city_picker/blob/main/screenshot/Screenshot2.jpg" width="240"/>
</div>
<img src="https://github.com/prof22/country_state_city_picker/blob/main/screenshot/Screenshot3.jpg" width="240"/>
<img src="https://github.com/prof22/country_state_city_picker/blob/main/screenshot/Screenshot4.jpg" width="240"/>
<img src="https://github.com/prof22/country_state_city_picker/blob/main/screenshot/Screenshot5.jpg" width="240"/>
<img src="https://github.com/prof22/country_state_city_picker/blob/main/screenshot/Screenshot6.jpg" width="240"/>
<img src="https://github.com/prof22/country_state_city_picker/blob/main/screenshot/Screenshot7.jpg" width="240"/>
<img src="https://github.com/prof22/country_state_city_picker/blob/main/screenshot/Screenshot1.jpg" width="240"/>

## Usage

To use this plugin, add `country_state_city_picker` as a [dependency in your pubspec.yaml](https://flutter.io/platform-plugins/).

```dart
     SelectState(
              onCountryChanged: (value) {
              setState(() {
                countryValue = value;
              });
            },
            onStateChanged:(value) {
              setState(() {
                stateValue = value;
              });
            },
             onCityChanged:(value) {
              setState(() {
                cityValue = value;
              });
            },
            
            ),
```

To call feedback or getting data from this widget, you can make function in onChanged

### Example

```dart
import 'package:flutter/material.dart';
import 'package:country_state_city_picker/country_state_city_picker.dart';

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  // This widget is the root of your application.
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      title: 'Country State and City Picker',
      theme: ThemeData(
        primarySwatch: Colors.blue,
        visualDensity: VisualDensity.adaptivePlatformDensity,
      ),
      home: MyHomePage(),
    );
  }
}

class MyHomePage extends StatefulWidget {
  
  @override
  _MyHomePageState createState() => _MyHomePageState();
}

class _MyHomePageState extends State<MyHomePage> {

  String countryValue;
  String stateValue;
  String cityValue;
  @override
  Widget build(BuildContext context) {
    
    return Scaffold(
      appBar: AppBar(
        title: Text('Country State and City Picker'),
      ),
      body:  Container(
        padding: EdgeInsets.symmetric(horizontal: 20),
        height: 600,
        child: 
         Column(
          children: [
            SelectState(
              onCountryChanged: (value) {
              setState(() {
                countryValue = value;
              });
            },
            onStateChanged:(value) {
              setState(() {
                stateValue = value;
              });
            },
             onCityChanged:(value) {
              setState(() {
                cityValue = value;
              });
            },
            
            ),
            // InkWell(
            //   onTap:(){
            //     print('country selected is $countryValue');
            //     print('country selected is $stateValue');
            //     print('country selected is $cityValue');
            //   },
            //   child: Text(' Check')
            // )
          ],
        )
      ),
    );
  }
}

```

### Special Thanks

- Salvatore Giordano, CountryCodePicker [CountryCodePicker](https://github.com/imtoori/CountryCodePicker)
- @tomrozb and @dev-fema for changelog 1.0.0+3
- @giaotuancse for changelog 1.0.0+4
- @joshuachinemezu for changelog 1.0.0+6 - 1.0.0+8
- @u-gin for chaangelog 1.0.0+9
- @imurnane for chaangelog 1.0.1+1
- @jpainam for chaangelog 1.0.1+2