---
title: Difference Between Const & Let Variables In Javascript
date: "2020-05-04"
description: Learn When to Use Const Over When to Use Let Variables In ES6 JavaScript. Learn Now!
---

If you are like me and found that when ES6 came out, you were scratching your head when you saw there were two new variable options, const and let. Since JavaScript is the first languauge I learned, I didn't know there were any other variables bindings out there except for var. If you had the same experience or are currently having this experience right now, please read on and learn the difference between const and let variables.

## What Is A Const Variable?
A const variable stands for "constant" meaning it cant change. Const variables were created because before ES6, we could change variables, and at anytime with both global and lexical scoping. This invited a lot of uninteded bugs in people's programs because people would create global variables and would accidentally change the variable later on down the road. Either because they forgot they already declared that variable name or because someone else working on the same project didn't know that global name existed. This was an issue for a long time.

`var salad = true;`

`salad = false;`

`console.log(salad); // false`

Well with const we can declare a variable as constant so that variable can never be changed, which is great!

`const salad = true;`

`salad = false;`

`console.log(salad) // console will throw a TypeError: Assignment to constant variable`

## What Is A Let Variable?
When I first saw a let variable I figured it replaced var and we never had to use it ever again. Now I realize that var and let are different, and var still has its place in JavaScript. With the creation of let, we can have more control over [lexical scoping](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Closures), which is great when we want to create closures, but can cause a lot of bugs.

Before let, if a variable was created inside of a conditional if/else statement, it could permanently change a global variable with the same name.

Imagine you enetered a drag race against someone driving a Tesla. You agreed to make six laps and whoever finished first, has to give up their pink slips. You both raced and you beat the other driver and won their Tesla! Well when it was time to process your new pink slip, the DMV software was outdated and was still using var instead of let in their code. Somehow a toy car was sent to your house instead of your new Tesla. See how this happened:


`var car = "Tesla";`

`if (car) {`

`var car = "toy car";`

`console.log(car); // toy car`

`}`

`console.log(car); // toy car`

See how var can be a huge issue by changing the car global binding from Tesla to toy car so easily, with only a few lines of code. 

This is where the let variable comes in handy.

`var car = "Tesla";`

`if (car) {`

`let car = "toy car"`

`console.log(car); // toy car`

`}`

`console.log(car); // Tesla`

## Conclusion
With the rollout of const and let variables, programmers have much more control over their program then only using var. If you ever forget what the difference is between let and var, just remember if you want a Tesla over a toy car, use let.