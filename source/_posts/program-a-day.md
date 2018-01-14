---
title: JavaScript-program-a-day
date: 2018-01-11 20:28:50
tags:
icon: fa-code
author: "Joshua Prpich"
---

A program a day keeps lazyness away! These are the JS examples I followed and learned from JS understanding the weird parts videos.

The first program I did was a Function Factory. 

{% codeblock lang:javascript %}
function makeGreeting(language){

  return function(firstname, lastname){


    if (language === "en") {
      console.log('Hello ' + firstname + ' ' + lastname)
    }

    if (language === 'es') {
      console.log('Hola ' + firstname + ' ' + lastname)
    }
  }

}

var greetEnglish = makeGreeting('en')
var greetSpanish = makeGreeting('es')

greetEnglish("joshua", "do")
greetSpanish("josue", "leguizamo")
{% endcodeblock %}

The second program I made was and example to practice closures and callbacks.


{% codeblock lang:javascript%}
function sayHiLater(){

  var greeting = "Hi!";

  setTimeout(function(){
    console.log(greeting)
  }, 3000)
}


sayHiLater();


function tellMeWhenDone(callback){
  var a = 1000; 
  var b = 2000;

  callback();
}


tellMeWhenDone(function(){
  console.log("I am done!")
});


tellMeWhenDone(function(){
  console.log("All is done!")
});
{% endcodeblock %}

