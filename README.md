# node-react-starterpack


step-by-step guide to the production below
* creating backend
    - create directory for the project
    - open terminal and change directory to the created project directory
    - set up the project configuration by type the following command on the terminal; (npm init -y)
    - install the required packages, thus:
        npm i express body-parser mysql2
        npm i -D nodemon
    - create a server.js file
    - add the code below to it
        // server.js

        const http = require('http');

        // Create an instance of the http server to handle HTTP requests
        let app = http.createServer((req, res) => {
            // Set a response type of plain text for the response
            res.writeHead(200, {'Content-Type': 'text/plain'});

            // Send back a response and end the connection
            res.end('Hello there! Welcome to the backend.\n');
        });

        // Start the server on port 3000
        app.listen(5000, '127.0.0.1');
        console.log('Node server running on port 5000');
    - add this two-line to "scripts" in package.json...
        "scripts": {
        ...
        "start": "node server.js",
        "start:dev": "nodemon server.js"
        },
        ...
    - run this command on the terminal
        npm run start:dev
    - create a db.js file
    - open a browser and go to http://localhost:5000
* creating frontend
    - First of all, create a frontend folder with your desired folder name and open a terminal on that folder, then run -
        npx create-react-app appName (in this case crud-frontend)
        cd appName
        npm start

frontend (using react) and backend (using node) have bn successfully created