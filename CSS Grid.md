## CSS Grid
The CSS grid is a newer standard that makes it easy to build complex responsive layouts. It works by turning an HTML element into a grid, and lets you place child elements anywhere within.

1. Create Your First CSS Grid
Turn any HTML element into a grid container by setting its display property to grid. This gives you the ability to use all the other properties associated with CSS Grid.

| In CSS Grid, the parent element is referred to as the container and its children are called items.


#### Add Columns with grid-template-columns
Simply creating a grid element doesn't get you very far. You need to define the structure of the grid as well. To add some columns to the grid, use the grid-template-columns property on a grid container as demonstrated below:

```
.container {
  display: grid;
  grid-template-columns: 100px 100px 100px;
  grid-template-rows: 50px 50px;
}
```

This will give your grid two columns that are each 50px wide. The number of parameters given to the grid-template-columns property indicates the number of columns in the grid, and the value of each parameter indicates the width of each column.


#### Use CSS Grid units to Change the Size of Columns and Rows
You can use absolute and relative units like px and em in CSS Grid to define the size of rows and columns. You can use these as well:

fr: sets the column or row to a fraction of the available space,
auto: sets the column or row to the width or height of its content automatically,
%: adjusts the column or row to the percent width of its container.

`grid-template-columns: auto 50px 10% 2fr 1fr;`
This snippet creates five columns. The first column is as wide as its content, the second column is 50px, the third column is 10% of its container, and for the last two columns; the remaining space is divided into three sections, two are allocated for the fourth column, and one for the fifth.

#### Create a Column Gap Using grid-column-gap
So far in the grids you have created, the columns have all been tight up against each other. Sometimes you want a gap in between the columns. To add a gap between the columns, use the grid-column-gap property like this:

`grid-column-gap: 10px;`
This creates 10px of empty space between all of our columns.

#### Add Gaps Faster with grid-gap
grid-gap is a shorthand property for grid-row-gap and grid-column-gap from the previous two challenges that's more convenient to use. If grid-gap has one value, it will create a gap between all rows and columns. However, if there are two values, it will use the first one to set the gap between the rows and the second value for the columns.

#### Align an Item Horizontally using justify-self
In CSS Grid, the content of each item is located in a box which is referred to as a cell. You can align the content's position within its cell horizontally using the justify-self property on a grid item. By default, this property has a value of stretch, which will make the content fill the whole width of the cell. This CSS Grid property accepts other values as well:

start: aligns the content at the left of the cell,
center: aligns the content in the center of the cell,
end: aligns the content at the right of the cell.
