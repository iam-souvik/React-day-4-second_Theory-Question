# React-day-4-second_Theory-Question
1.State vs Props Ans : State is the local state of the component which cannot be accessed and modified outside of the component. It's equivalent to local variables in a function. Props, on the other hand, make components reusable by giving components the ability to receive data from their parent component in the form of props

State : The state is a data structure that starts with a default value when a Component mounts. It may be mutated across time, mostly as a result of user events.A Component manages its own state internally. Besides setting an initial state, it has no business fiddling with the state of its children. You might conceptualize state as private to that component.

Props : Props (short for properties) are a Component's configuration. They are received from above and immutable as far as the Component receiving them is concerned. A Component cannot change its props, but it is responsible for putting together the props of its child Components. Props do not have to just be data -- callback functions may be passed in as props.

Usestate API
Ans: UseState API useases

const [value,setvalue] = useStae([]) returns a stateful value, and a function to update it.

3.Explain the how map, filter, reduce work

Ans : map:Map require a callback function, basically map function map through the all the array and returns a array like if we have to update all our array elements to by sum of two in this case we must use map and in callback function we can pass the condition and we can able to get the new array,

filter: filter also accept the callback function it can filter the whole array and return a new array with the filtered value lets suppose we have to find all even number in a array in this case we must use filter methode to filter the array and to get the desirable output.

reduce :Reduce is also a heigher order function.It also accept the calback function. It require two things like the initial value and with the intial value it add all elements in an array and lastly calcularte sum of the total elements in an array.

3.arr.map prototype methode

Array.prototype.myMap=function(myFunction){ let newArr = []; for(let i = 0;i<this.length;i++){ let a = myFunction(this[i]); newArr.push(a) } return newArr }

arr.filter prototype methode;

Array.prototype.myFilter= function(myfunction){ let newArr = []; for(let i = 0;i<this.length;i++){ if(myfunction(this[i])){ newArr.push(this[i]) } } return newArr }

arr.reduce prototype methode;

Array.prototype.myReduce = function(myfunction){ let sum = 0; for(let i = 0;i<this.length;i++){ let a = myfunction(sum,this[i]); sum = a; } return sum; }




let x = arr.myMap(function(el){
    return el*2
})
console.log(x)
let w = arr.myReduce(function(total,value){
    return total+value
})
console.log(w)
let z = arr.myFilter(function(el){
    return el%2==0;
})
console.log(z)