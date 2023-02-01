## HOW WE CREATED THIS :
0. Vocabulary
    1. Create ( file, folder ...)
    2. Add ( fct, class, script ...)
    3. COPY ( file, fct ...)
    3. Run ( cmd in terminal )


1. Install dev tools
    1. node & npm
    2. yarn
    3. git

2. Initialising the project : Setting Up Node and TS
    1. RUN *npm init -y*
    2. RUN *yarn add -D @types/node typescript* >> setUp TS & get node & TS to work together
        --> @types/node: This package provides type definitions for Node.js, which can be used with TypeScript to improve development experience and catch type errors at compile time.
        --> typescript: This is the TypeScript compiler, which allows you to write TypeScript code that gets transpiled to JavaScript.
    3. RUN *yarn add -D ts-node*  >> ts-node allows you to run TypeScript directly from the command line without compiling it to JavaScript first.
    4. Add *"start":"ts-node src/index.ts"* to the scripts in **package.json** >> so we can run *yarn start* or *npm run start*.
    5. Create *src/index.ts*
    6. COPY *tsconfig.json* File from **benawad**
        --> A TypeScript configuration file (tsconfig.json) is used to specify the compiler options for your TypeScript project. It allows you to customize the behavior of the TypeScript compiler and helps ensure that all developers working on the project are using the same configuration.
        --> What can it do ?
            _ Specifying the version of TypeScript that you want to use
            _ Setting the target JavaScript version for the compiled code
            _ Configuring the type checking behavior
            . . . 
    7. Add *"watch":"tsc -w"* to the scripts in **package.json** >> so we can run *yarn watch* or *npm run watch*
        --> The script runs the TypeScript compiler (tsc) with the -w flag, which stands for "watch". The -w flag causes the TypeScript compiler to watch for changes in your TypeScript files and re-compile them whenever a change is detected.
        --> yarn start is slow compared to this approach
    8. Add *"start":"node dist/index.js"*  &&  change old start script to *"start2":"ts-node src/index.ts"*
    9. RUN *yarn add -D nodemon*
    10. Add *"dev":"nodemon dist/index.js"*
    11. OPTIONALY ADD *"dev2":"nodemon --exec ts-node src/index.ts"*
    12. RUN *yarn watch* >> OPEN new terminla >> RUN *yarn dev*