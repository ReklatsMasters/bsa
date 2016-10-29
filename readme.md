# bsa
> Bethesda Softworks Archive compress/decompress

## Example

```js
const bsa = require('bsa')
const fs = require('fs')

const file = fs.readFileSync('Skyrim - Interface.bsa')
console.log(bsa.list(file))

/*
output:

[ 'interface\\controls\\360\\keyboard_english.txt',
  'interface\\controls\\360\\gamepad.txt',
  'interface\\controls\\360\\controlmap.txt',
  'interface\\controls\\ps3\\keyboard_english.txt'
  // more other files...
]
*/
```

## API

#### `list(buf: Buffer): Array<string>`
Return the list of files with folders names in archive

#### `extract(buf: Buffer, where: string(default = '.')): Promise<>`
extract files

## License
MIT, 2016 (c) Dmitry Tsvettsikh
