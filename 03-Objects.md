# Objects or Prototypes

Example of a Object

```javascript
const backpack = {
  name: "Everyday Backpack",
  volume: 30,
  color: "grey",
  pocketNum: 15,
  strapLength: {
    left: 26,
    right: 26,
  },
  lidOpen: false,
  toggleLid: function (lidStatus) {
    this.lidOpen = lidStatus;
  },
  newStrapLength: function (lengthLeft, lengthRight) {
    this.strapLength.left = lengthLeft;
    this.strapLength.right = lengthRight;
  },
};
```

## Accessing methods

- Dot notation: ```object.value```
- Braket notation: ```object["value"]```

to prevent error ```typeof object.value != 'undefined'```

**To Print**
```console.log("key:",object.value);```

## Clasess | Object Blueprints

```javascript
class Filter{
    constructor(){
        this.records = [];
    }

    set(record){
        this.records.push(record);
    }

    delete(key){
        //...
    }
}

export default Filter;
```

## Global Objects

Reference: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects
