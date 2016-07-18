# react-native-smart-sudoku-grid

A sudoku grid layout for react-native apps. Written in JS for cross-platform support.
It works on iOS and Android.

This component is compatible with React Native 0.25 and newer.

## Preview

![react-native-smart-sudoku-grid-preview][1]

## Installation

```
npm install react-native-smart-sudoku-grid --save
```

or

```
npm install @react-native-component/react-native-smart-sudoku-grid --save
```

## Usage

Install the button from npm with `npm install @react-native-component/react-native-smart-sudoku-grid --save`.
Then, require it from your app's JavaScript files with `import Button from '@react-native-component/react-native-smart-sudoku-grid'`.

```js

```

## Props

Prop            | Type   | Optional | Default     | Description
--------------- | ------ | -------- | ----------- | -----------
rowWidth        | number | Yes      | deviceWidth | determines the width of a row.
columnCount     | number | No       |             | determines how many columns a row contains.
dataSource      | array  | No       |             | determines the datasource of grid
renderCell      | func   | No       |             | A function that returns the grid cell component.
containerStyle  | style  | Yes      |             | see [react-native documents][2]


[1]: http://cyqresig.github.io/img/react-native-smart-sudoku-grid-preview-v1.0.0.gif
[2]: https://facebook.github.io/react-native/docs/style.html