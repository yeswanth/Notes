### Principles
* **First principle:** Every thing that changes in javascript application including data and UI will be contained in a single object called state or state tree 
* **Second principle:** State is redundant. State can be changing by dispatching actions. All action will have a type parameter 
* **Third principle:** Reducer functions have to be pure with the following input and output  
```
Input - previous state + action dispatched 
Output - next state 
```
* If a reducer is passed an action that it does not understand, it should return current state of the application 
* If a reducer is sent undefined as the state, it MUST return what it considers to be initial state of the application 


### Pure vs Impure functions 
Pure functions won’t have any observable side effects (like network and database)
Pure functions don’t modify values passed to them 
Pure functions will return the same result if the same input that is passed to them 

###Implementation 
```
const counter  = (state = 0,action) => {
	switch(action.type){
	     case ‘INCREMENT’:
            return state + 1;
       case 'DECREMENT':
            return state - 1;
       default:
            return state;
}
}
```
