# Jeux-Undo

Adds undo and redo to Jeux applications

## Installation


```bash
npm install jeux-undo
```

## Usage

```javascript
import {undoRedo} from "jeux-undo"

// counter reducer
function counter (state = 0, action){
    if(action.type ==="INC"){
        return state + 1
    }
    if(action.type === "DEC"){
        return state - 1;
    }
    return state;
}

export undoCounter = undoRedo(counter);


// seperate file
// instance of jeux store
// mock state
const state = {
    counter: 0
}
store.dispatch({type : "INC"})
// state.counter has a value of 1
store.dispatch({type : "UNDO"})
// state.counter has a value of 0

```

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License
[MIT](https://choosealicense.com/licenses/mit/)