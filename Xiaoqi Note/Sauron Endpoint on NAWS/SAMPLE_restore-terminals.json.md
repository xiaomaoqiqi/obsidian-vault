

{

"artificialDelayMilliseconds": 300,

"keepExistingTerminalsOpen": false,

"runOnStartup": true,

"terminals": [

{

"splitTerminals": [

{

"name": "server",

"commands": ["npm i", "npm run dev"]

},

{

"name": "client",

"commands": ["npm run dev:client"]

},

{

"name": "test",

"commands": ["jest --watch"]

}

]

},

{

"splitTerminals": [

{

"name": "build & e2e",

"commands": ["npm run eslint", "npm run build", "npm run e2e"],

"shouldRunCommands": false

},

{

"name": "worker",

"commands": ["npm-run-all --parallel redis tsc-watch-start worker"]

}

]

}

]

}


