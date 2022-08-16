# Css Grid

    // grid-based rules
    @supports not (display: grid) {
    // float-based rules
    }

## Grid Property

align-content align-items align-self grid grid-area
grid-auto-columns grid-auto-flow grid-auto-rows grid-column
grid-column-end grid-column-gap grid-column-start grip-gap
grid-row grid-row-end grid-row-gap grid-row-start
grid-template grid-template-area grid-template-columns
grid-template-rows justify-content justify-items
justify-self order

<note> pick the one not familar with

-   align-self ?
-   justify-self?
-   grid-auto-columns vs grid-auto-flow vs grid-auto-rows

layout

-   Grid cells  
-   Grid columns
-   Grid rows
-   **Grid tracks**
-   Grid lines
-   Grid areas
-   **Grid items**
-   Gaps
-   Margins

## Two-Step Grid process

    [grid container] {
    grid-template-columns: 200px 200px;
    grid-template-columns: 1fr min-content minmax() fit-content...
    }

- grid-template-columns: defines the number of columns in a grid container and their widths

- display: grid **makes an element into a grid container**

### Changing the Position of Grid Items

-   grid-column-start 
-   grid-column-end

        grid-column-start: [grid line]

### Grid Rows and the Implicit Grid

        [grid container] {
        grid-template-rows: [track sizes];
        grid-template-rows: min-content 200px 200px;
        }
- grid-template-rows : define the number of rows in a grid container and their height

- min-content : define a track size which is large enough to hold its content, but not larger

## Define Grids: in-depth

### Grid Track Sizes

- static values
- percentage
- auto
- fr : fractional unit, divide up the remaining space
- min-content, 
- max-content : make track as large as necessary to contain its content
- minmax() : function to specify min and max value for a track
- fit-content() : fit track size to the content, but don't go above specified value
- repeat(number, track sizes): function to repeat a pattern of track sizes multiple times
- grid-auto-flow: whether the grid fills rows or columns first while assigning grid items (default: row)
- grid-auto-rows: the size of any implicitly-created rows
- auto-flow: keyword added to the grid shorthand property which determine the axis new tracks are added implicitly, and their size
- Viewport-responsive vs Content-responsive

|Percentage  |    min-content|
|fr          |    max-content|
|auto        |    fit-content()|

    grid-template-columns: 1fr minmax(max-content, 50%) 1fr;
    grid-template-columns: 1fr fit-content(30em) fit-content(30em) 1fr;
    grid-template-columns: repeat(3, 20em);
    grid-template: 20em 10em / repeat(6, 1fr);
    grid-auto-flow: column;
    grid-auto-rows: 10em;
    grid: 10em 10em / auto-flow 10em
    grid-column-gap: 1em;

### implicit grid

The columns and rows css grid creates itself to accommodate your grid items

## Positioning Items: in-depth

- span: instructs a grid item to span a certain number of tracks
- grid-column: define column-start and grid-column-end at once
- grid-row: define row-start and row-end at once
- grid-area: complete defind an item's position in one property
    
        grid-column-end: span 2;
        grid-column: 1 / 3;
        grid-row: 2 / 6;
        grid-area: 1 / 2 / 3 / 6;
        grid-auto-flow: dense rows;
        z-index: 1;

### Alignment and Justification: Concept

- start(default)
- center
- end
- space-around
- space-between
- space-evenly


- dense: keyword added to grid-autoflow property which will flow items into the first empty grid area
- order: defines a different order for a grid item than its source order

