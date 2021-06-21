# React Drag and Drop Files


[![Version](http://img.shields.io/npm/v/react-drag-drop-files.svg)](https://www.npmjs.org/package/react-drag-drop-files) [![code style: prettier](https://img.shields.io/badge/code_style-prettier-ff69b4.svg)](https://github.com/prettier/prettier) [![npm download][download-image]][download-url] 

[download-image]: https://img.shields.io/npm/dm/react-drag-drop-files.svg?style=flat-square
[download-url]: https://npmjs.org/package/react-drag-drop-files


Light and simple reactjs drag and drop library.


## Demo

[![Edit react-drag-drop-files](https://codesandbox.io/static/img/play-codesandbox.svg)](https://codesandbox.io/s/react-drag-drop-files-sghbp)
## Installation
Install it from npm (using [NPM](http://webpack.github.io/)).

```bash
npm i --save react-drag-drop-files
```


## Usage
Using react hooks just as simple as:

```jsx static
import React, { useState } from "react";
import { FileUploader } from "react-drag-drop-files";

const fileTypes = ["JPG", "PNG", "GIF"];

function DragDrop() {
  const [file, setFile] = useState(null);
  const handleChange = file => {
    setFile(file);
  };
  return (
    <FileUploader 
        handleChange={handleChange} 
        name="file" 
        types={fileTypes} 
    />
  );
}

export default DragDrop;
```

## Options


Option | Type | Description | value example
--- | --- | --- | ---
name | string | the name for your form (if exist) | ```"myFile"```
classes | string | string with the classes wished to add | ```"drop_area drop_zone"```
types | Array<strings> | array of strings with extentions to check and go throw | ```['png', 'jpeg', ...]```
onTypeError | function | function that will be called only of error occured related to type | ```(err) => console.log(err)```
children | JSX Element, any | if you want to replace the current design inside the box of drop zone. | ```<div><p>this is inside drop area</p></div>``` or just text
maxSize | number | the maximum size of the file (number in mb) | 2
minSize | number | the minimum size of the file (number in mb) | 1
onSizeError | function | function that will be called only of error occured related to size min or max | ```(file) => console.log(file)```
onDrop | function | function that will be called when the user drop a file on the drop area only | ```(file) => console.log(file)```
onSelect | function | function that will be called when the user select a file on click the file area only | ```(file) => console.log(file)```
handleChange | function | function that will be called when the user select or drop a file | ```(file) => console.log(file)```

### Upcoming...

- [x] Files Validation
- [ ] Adding Multiple Files
- [ ] Testing
- [x] Typescript Support
- [ ] Contribution Guide
- [x] Show different type of Errors
## License
[MIT](https://choosealicense.com/licenses/mit/)
