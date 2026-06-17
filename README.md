# lwc-my-practice-
my practise code of lwc
-----------------------------html---------------------------
<template>
    <div class = "helloWorld" ></div>
    <lightning-card  title ="Hello World !" >
        <header> Header </header>
        <p>Hi, {greeting}!!! </p>
        <lightning-input  label="Enter you name " value = {greeting} onchange ={changeHandler}  ></lightning-input>  
        </lightning-card>  
</template> 
----------------------------js-------------------------------
import { LightningElement } from 'lwc';
    export default class helloWorld extends LightningElement{
    
        greeting = 'enter your name here ';
        changeHandler (event){
            this.greeting = event.target.value;
        }    
}
-----------------------------meta---------------------------------
<?xml version="1.0" encoding="UTF-8"?>
<LightningComponentBundle xmlns="http://soap.sforce.com/2006/04/metadata" fqn="helloWorld">
    <apiVersion>63.0</apiVersion>
    <isExposed>true</isExposed>
    <targets>
    <target>lightning__AppPage</target>
    <target>lightning__RecordPage</target>
    <target>lightning__HomePage</target>
    </targets>
</LightningComponentBundle>
