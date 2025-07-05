# Convert array of object into object
```js
const carsInfo = [
  {
    name: "punch",
    color: "grey",
    brand: "tata",
  },
  {
    name: "tiago",
    color: "white",
    brand: "tata",
  },
  {
    name: "verna",
    color: "red",
    brand: "hyundai",
  },
]
//{tata: ["punch","tiago"], Hyundai:["verna"]}
const resultObj = carsInfo.reduce((acc,car)=>{
(acc[car.brand] =  acc[car.brand] || []).push(car.name)
return acc
},{})
console.log("resultObj", resultObj)

```
