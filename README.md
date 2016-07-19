# react-native-smart-sudoku-grid

A smart sudoku grid layout for react-native apps. Written in JS for cross-platform support.
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
const dataList = [
  {
    icon: image_cash,
    title: 'cash',
  },
  {
    icon: image_credit,
    title: 'credit',
  },
  {
    icon: image_transfer,
    title: 'transfer',
  },
  {
    icon: image_loan,
    title: 'loan',
  },
  {
    icon: image_charge,
    title: 'charge',
  },
  {
    icon: image_payment,
    title: 'payment',
  },
  {
    icon: image_shopping,
    title: 'shopping',
  },
  {
    icon: image_service,
    title: 'service',
  },
  {
    icon: image_donate,
    title: 'donate',
  },
]

const columnCount = 3

export default class ThreeColumns extends Component {

  render() {
      return (
          <ScrollView style={{marginTop: 44 + 20, backgroundColor: '#fff', }}>
            <View style={{height: 30, paddingLeft: 10, backgroundColor: '#E1E5E8', justifyContent: 'center', }}>
              <Text>Services: </Text>
            </View>
            <SudokuGrid
              containerStyle={{ backgroundColor: '#fff',}}
              columnCount={columnCount}
              dataSource={dataList}
              renderCell={this._renderGridCell}
            />
          </ScrollView>
      )
  }

  _renderGridCell = (data, index, list) => {
      return (
          <TouchableHighlight underlayColor={'#eee'} onPress={ this._onPressCell.bind(this, data, index) }>
            <View style={{justifyContent: 'center', alignItems: 'center', height: 100,
                          borderBottomWidth: StyleSheet.hairlineWidth, borderColor: '#eee',
                          borderRightWidth: (index + 1) % columnCount ? StyleSheet.hairlineWidth: 0, }}>
              <Image source={data.icon} style={{width: 30, height: 30, marginHorizontal: 10, marginBottom: 10,}}/>
              <Text>{data.title}</Text>
            </View>
          </TouchableHighlight>
      )
  }

  _onPressCell(data, index) {
      Alert.alert('clicked ' + data.title)
  }

}
```

## Props

Prop            | Type   | Optional | Default     | Description
--------------- | ------ | -------- | ----------- | -----------
rowWidth        | number | Yes      | deviceWidth | determines the width of a row.
columnCount     | number | No       |             | determines how many columns a row contains.
dataSource      | array  | No       |             | determines the datasource of grid
renderCell      | func   | No       |             | A function that returns the grid cell component.
style           | style  | Yes      |             | see [react-native documents][2]


[1]: http://cyqresig.github.io/img/react-native-smart-sudoku-grid-preview-v1.0.0.gif
[2]: https://facebook.github.io/react-native/docs/style.html