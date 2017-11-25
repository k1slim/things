## Right import to reduce bundle size
Example:
```js
import Nav from 'react-bootstrap/lib/Nav';
```
Pay attention that following import will include whole lib:
```js
import {Nav, NavItem} from 'react-bootstrap';
```

This works for libs below:
- react-bootstrap
- react-color

## Search in arrays vs objects

```js
let letters = 'abcdefghqw';
letters = letters.split('');

const arr = letters.map(item => ({
    props: item
}));

const obj = [];
letters.map(item => obj[item] = { prop: item });

function checkTime(value) {
    console.time('Object');
    const findInObject = obj[value];
    console.timeEnd('Object');
    console.time('Array');
    const findInArray = arr.find(i => i.prop === value);
    console.timeEnd('Array');
}

checkTime();
```

##Promises
```js
// TODO
```