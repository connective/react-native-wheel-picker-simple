# React Native Wheel Picker Simple

![](https://img.shields.io/npm/v/react-native-wheel-picker-simple)
![](https://img.shields.io/npm/l/https://img.shields.io/npm/v/react-native-wheel-picker-simple)

A simple Wheel Picker, rendered with native components on Android and iOS. For iOS, pickerIOS is used. Forked from [react-native-wheel-picker-android](https://github.com/KalonTech/ReactNativeWheelPicker).

![](https://img.shields.io/badge/-feature-blue) This picker works inside scrollViews.


## Installation
`yarn add react-native-wheel-picker-simple`

![screencast](screencast.gif)

## Usage

```js
<View style={wheelPickerWrapperStyle}>
  <WheelPicker
    itemStyle={{
      marginTop: -30,
      backgroundColor: '#111111',
      color: '#EEEEEE',
      fontSize: 12,
      fontFamily: "YourFontName"
    }}
    selectedItemTextFontFamily={'YourFontName'}
    itemTextFontFamily={'YourFontName'}
    selectedItemTextSize={12}
    itemTextSize={12}
    selectedItemTextColor={'#EEEEEE'}
    indicatorColor={'#999999'}
    selectedItem={selectedIndex}
    data={onAddItem ? itemsModified : items}
    onItemSelected={this.onItemSelected} />
</View>

```

## iOS Specific style

`itemStyle` prop is applied only to iOS.


## Android Specific style

You can add styles conditionally based on OS

```js
let wheelPickerWrapperStyle = [gs.centerChildren, gs.row, gs.centerAlongFlex];
if(Platform.OS === 'android')
  wheelPickerWrapperStyle.push(s.wheelPickerWrapperAndroid;
```

For more info, please refer to the parent [repo](https://github.com/KalonTech/ReactNativeWheelPicker)

## Limitations

- iOS Date Picker is not customizable i.e. background color, fonts, etc. cannot be changed. No dark theme 😞

- iOS Picker line color cannot be changed 😟. At least it looks and feels okay in iOS, unlike the date picker.

## Contribution
**Issues** are welcome. Please add a screenshot, if not screencast, of bug and code snippet. Quickest way to solve issue is to reproduce it on one of the examples.

Pull requests are very welcome.

1. Fork the repo
1. Create new branch with feature name as branch name
1. Check if things work with a jupyter notebook
1. Raise a pull request

## Licence

Please see attached [Licence](LICENCE)
