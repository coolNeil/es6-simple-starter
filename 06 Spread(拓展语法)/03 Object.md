# Object

```js
const cars = {
    ford: 'american',
    audi: 'german',
    saab: 'swedish'
};

const oldCars = {
    morgan : 'British'
};

const vehicles = {
    ...cars,
    ...oldCars
}; //Same as Object.assign({}, cars, oldCars)

const newVehicles = {
    ...vehicles,
    ford: 'japanese'
}; //Same as Object.assign({}, cars, {ford: 'japanese'})
```