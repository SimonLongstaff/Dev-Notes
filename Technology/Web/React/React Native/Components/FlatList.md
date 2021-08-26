# Flat List
List optimized for rendering long list of react components / items

## Arguments
- Data => Required prop consisting of the items to be displayed in a liost
- renderItem => Required prop function that tells the list how to render each item


### renderItem destructuring
You can use deconstruction when using render item instead of passing it element because element looks like this
`renderItem={(element) => {}}`
`element = {item: {field1: ---, field2:----}, index:0}`

instead used

`renderItem={({item}) => {}`
`item = {field1: ---, field2:----}`

### keyExtractor
Use keyExtractor function to get keys for a list

`keyExtractor={item => item.name}`