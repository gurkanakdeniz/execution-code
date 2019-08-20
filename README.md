<img align="left" width="170" src="sketch/kicket-logo.png" />

# Rest API Playground [![Build Status](https://travis-ci.com/gurkanakdeniz/kicket.svg?branch=master)](https://travis-ci.com/gurkanakdeniz/kicket)

# Why we did that?

> Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.

# What's happening on inside?

<div align="center">
    <img width="75%" src="sketch/kicket-raw.drawio.png" />
</div>
<hr/>

### Let's look at step by step;

> When user want to deploy API

###### Request hit to our '/create' endpoint with the platform chosen by the user. kicket forward the request to related application server. If related application server doesn't send any error to kicket, kicket insert user's API platform and API UUID that generated by the related application server. In this way, we validate user's API platform. Finally, we return the UUID to user to call their API.

> When user want to run exist API

###### Request hit to our '/run' endpoint with the UUID. Firstly,kicket check this UUID in MongoDB, if kicket find this UUID, kicket get the platform information to forward the request. After request forward to related platform, request have 5 seconds to return some response. API's response or timeout response return to user directly.

### How can I build & run the project locally?

1. You can clone only [kicket](https://github.com/gurkanakdeniz/kicket) repository.

   - You need to MongoDB and Node JS(> v12.5.0)
   - In this case, you need to change .env file.
   - Your .env file look like;
     - JAVA_API=http://localhost:8080
     - NODE_API=https://kicket-node.herokuapp.com
     - PYTHON_API=https://kicket-python.herokuapp.com
     - PHP_API=http://localhost:5000
     - HTML_API=http://localhost:3004
     - GO_API=https://kicket-go.herokuapp.com
     - MONGO=mongodb://localhost:27017/execode
   - Type your terminal npm install & npm start.

2. You can clone [kicket](https://github.com/gurkanakdeniz/kicket) repository and all dependent projects(repository links are below). In this case, you don't touch any files just type your terminal npm install then, npm start.

### In Progress Main Functionality

- All programming language supports get exist API with UUID and update.

###### You can help us to solve kicket's issue, or feel free to open new issue if you realize some bugs, check [here.](https://github.com/gurkanakdeniz/kicket/issues)

### Dependent projects

- [Java Repository](https://github.com/gurkanakdeniz/kicket-java)
- [Node JS Repository](https://github.com/ilkemerol/kicket-node)
- [HTML Repository](https://github.com/ilkemerol/kicket-html)
- [Pyhton Repository](https://github.com/gurkanakdeniz/kicket-python)
- [Golang Repository](https://github.com/gurkanakdeniz/kicket-go)
- [PHP Repository](https://github.com/gurkanakdeniz/kicket-go)