# BASliderView
BASliderView is a customizable bottom slide Menu.
# Compatibility
BASliderView requires iOS 10+ and is compatible with Swift 4.2 projects.
# Installation
Drag and Drop the folder `Source` into your project.
# Usage

BASliderView was designed to be used effortlessly.

## Create Cells
create the cells as follows:- 
```swift
        let cell1 = BASliderViewCellProperties(
            nibName: BASliderViewCellIdetifiers.imageCell.rawValue,
            cellIdentifier: BASliderViewCellIdetifiers.imageCell,
            index: 1,
            itemProperties: [BASliderItemProperties(
                itemID: 10001,
                text: "",
                font: UIFont.systemFont(ofSize: 12, weight: .regular),
                textColour: .black,
                textAlignment: .center,
                backgroundColour: .white,
                desiredHeight: 50,
                imageName: "icCross"
            )]
        )
```
we have diffrent types of default cell types: 
```
headerCell
buttonCell
twoButtonCell
imageCell
textCell

```
### As per requirements, we can define our own cells.
####  How?
1. Create a tableView cell with .xib
2. Assign `BASlideViewDefaultTableViewCell` as tableview cell `class`
3. Override `itemProperties`
4. Your new cell is ready.


## Presenting

Once you completes creating cells, make an array of  `[BASliderViewCellProperties]`.

```swift
        let sliderViewCells = [cell1, cell2, cell3, cell4]  // [BASliderViewCellProperties]
```
then,
```swift
        BASlider.show(title: "Alert", sliderViewCells: sliderViewCells, dismissOnTap: true, isHeaderEnabled: true, controller: self)
```

GOOD LUCK
## Authors

[Betto Akkara](https://github.com/bettoakkara)

## License

<b>BASliderView</b> is released under a MIT License. See LICENSE file for details.

