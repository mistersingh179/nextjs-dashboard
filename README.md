# Learning Next.js v14.x with app folder over previous api & page folder

### css modules
- make css file a module like `foo.module.css` then import it like `import styles from './foo.module.css'`
- now every class inside foo is given back with a unique name for the module it is being imported from.
- this way `.home` class in `foo` will not mess up another `.home` class in another file.

### clsx
- use it to apply classes conditionally
- more concise than ternary as don't have say `""` when it is false and class does not need to be applied. 

### next/font
- use this package to load google fonts
- this gets the fonts and stores them locally
- then uses them locally to avoid fetch at run time and eliminate cls

### layout and pages
- each folder is a route
- in each folder add `page.tsx` to export what is built on that route
- and each folder can have `layout.tsx` which will get as `children` any page which is rendered from within that folder.
- common practice is to use root layout for adding meta tags, modifying html, body tags and add stuff which should go everywhere.

### use client;
- by default every component is server side rendered
- so if it needs to access hooks, browser apis or have event handlers etc. then we need to explicity mark it a client component
- this is done by adding `"use client";` to the top of the component file.


