# React-Routing-Demo-App
React Js

Redux Steps

Package

npm install redux react-redux

import {createStore}  from 'redux';

function reducer(){
    return 'Rajendra';
}
const store=createStore(reducer);

console.log(store.getState());
-------------------------------------------------------------------
Version 2

import {createStore}  from 'redux';

function reducer(state,action){
    console.log(action);
    if(action.type==='ChangeName'){
         return action.payload.newstate; 
    }
    return 'Rajendra';
}
const store=createStore(reducer);

console.log(store.getState()); //output Rajendra

const action={
    type:'ChangeName',
    payload:{
        newstate:'Rajendra Taradale'
    }
};

store.dispatch(action);
console.log(store.getState());// output Rajendra Taradale



