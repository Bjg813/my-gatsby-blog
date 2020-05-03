---
title: Working With ES6 Modules
date: "2020-05-03"
description: Working With React Can Be Difficult If You Don't Understand ES6 Modules. Take A Quick Dive Into ES6 Modules & Save Time Now!
---

I just started working in React this month and didn't understand why I had to export and import components before I could use them. I didn't even know import and export were actually a new JavaScript feature that was debuted with ES6. After finally picking up a book on learning react by Orielly, did I finally realize modules are within ES6. Please follow along and learn about ES6 modules.

## What Is A JavaScript Module Anyway?
JavaScript modules were created so developers could reuse code in their projects and they are stored in seperate files where they can be imported and exported. 

Think of a time when you created a constructor or a variable that you wanted to use in other parts of your project but you couldn't without making them global. There were workarounds like incorporating a library, but there wasn't anything you could do within the languauge. Well now you can export and import pieces of code to keep your project DRY and resuable.

## Export Your Module
If you have dabbled in React, then you have seen "export" at the bottom of each page. If you are like me and realized this was the only way you could get your component to work across your app and just wrote export to get it to work, then we are on the same boat. 

Export is used to export modules so they can be used in another module. You can export a module by simply typing **export** at the bottom of your file or in front of any type (primitives, objects, arrays, functions). You can also type **export defualt**. I saw both were used in React and I wasn't really sure why we used default.

There are only two ways you can export a module, and that is with the export statement or the export default statement. 

If you want to export **multiple** types from a single module, use **export**.

If you want to export a **single** type from a modlue, use **export default**.

Easy as that:

**Export (multiple type)**

`./house-hold.js`

`export const person = {
    firstName: 'Brennan',
    lastName; 'Grout'
}
`

`export const animal = {
    species: 'Canine',
    name: 'Bingo'
}
`

**Export default (single type)**

`./pet.js`

`export default const rover = new Dog('Rover', 100, 'Ruff Ruff');`

## Import Your Module
Modules can be used in other JavaScript files by using the `import` statement. 

An important concept to realize is if you are importing multiple exports, you can destructure the exports you want and leave the rest, which is great for speed and size! If you are just importing a default export then you can't desctructure it, obviously, geez.

We list the import at the top of the file and type:

 `import typeName from 'fileName'`

`import { person, animal } from './house-hold.js`

`import rover from './pet.js'`

This is not all you can do with import though. You can also scope module variables locally, as in you can take a global variable and scope it to make it a local variable.

`import { person as p, animal as a } from './house-hold.js'`

In addition, you can import everything at once using the star * variable.

`import * as fns from './house-hold.js'`

**Note:** Modules is not supported by all browsers yet, so make sure you are using Babel in your project.