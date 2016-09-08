# CPSC 310 Project

This is the base project for CPSC310. Using it will help you get started with many of the tools we will use this term.

### Configure Environment

To start using this project you need to get your computer configured so you can build and execute the code. To do this, follow these steps; the specifics of each step (especially the first two) will vary based on which operating system your computer has:

1. Install git (you should be able to execute ```git -v``` on the command line).

1. Install Node, which will also install NPM (you should be able to execute ```node -v``` and ```npm -v``` the command line).

1. It is important that your project directory be called ```cpsc310project``` if you want to work with the public test suite we are providing. The easiest way to do this is to:
  
 * Clone the project: ```git clone git@github.com:CS310-2016Fall/cpsc310project_teamXXX.git``` (where ```XXX``` is your team number)
 
 * Move it to the right name: ```mv cpsc310project_teamXXX cpsc310project``` (again replacing ```XXX```)


### Prepare project

Once your project is configured you need to further prepare the project's tooling and dependencies. In the ```cpsc310project``` folder:

1. ```npm run clean```

1. ```npm run configure```

1. ```npm run build```

### Run unit tests

The sample project ships with some automated unit tests. These commands will execute the suites:
 
* Test: ```npm run test``` (or ```npm test```)
* Test coverage: ```npm run cover``` HTML reports: ```./coverage/lcov-report/index.html```

You can also run the tests as a Mocha target inside your favourite IDE (WebStorm and VSCode both work well and are free for academic use).

### Run integration tests

See the [cpsc310d1-pub](https://github.com/CS310-2016Fall/cpsc310d1-pub) repo for instructions.

### Start the server (for use with UI)

* ```npm run start``` (or ```npm start```)

See the [cpsc310-ui](https://github.com/CS310-2016Fall/cpsc310ui) repo for instructions.

### Developing the system

If you are developing in Typescript you will have to re-compile the Typescript code. This can be done with ```npm run build``` to build the system and get it ready to execute. New unit tests can be written and added to ```/test```; as long as the tests end in ```Spec.ts``` they will be executed automatically when you run ```npm run test```.

### Running and Testing in the IDE

While these instructions are for WebStorm, other IDEs (e.g., VSCode, Atom, etc.) and editors (e.g., Sublime) should be similar, or will at least be compatible with the command line options described above.

To run or test the system in WebStorm you will need to configure run targets. To run the system go to the ```Run->Edit Configurations``` and tap on the ```+``` and then ```Node.js```. Point the 'JavaScript file' argument to ```src/App.js```. To run the system tests, go to the ```Run->Edit Configurations``` and tap on the ```+``` and then ```Mocha```. Point the 'Test Directory' file argument to ```test/```.


