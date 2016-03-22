# most-web-jade
Most Web Framework Jade View Engine

![MOST Web Framework Logo](https://www.themost.io/assets/images/most_logo_sw_240.png)

A view engine for [jade](https://github.com/pugjs/pug) templates which are going to be used in web applications based on [MOST Web Framework](https://github.com/kbarbounakis/most-web)

## Install

$ npm install most-web-jade

## Usage

Register view engine by adding the following node in config/app.json engines collection:

    "engines": [
        ...
        {
            "name": "Jade View Engine", "extension": "jade", "type": "most-web-jade"
        }
        ...
        ]
    }

Create a new controller (app/controllers/example-controller.js):

    var web = require("most-web"), util = require("util");

    function ExampleController() {
        ExampleController.super_.call(this);
    }

    util.inherits(ExampleController, web.controllers.HttpBaseController);

    ExampleController.prototype.hello = function(callback) {
        return callback(null, this.result({ name:"Thomas" }));
    }

Create a jade template:

    h1 This is a Jade template
    h2 Hello #{data.name}

and place it in views folder:

    app
        + views
            + example
                hello.html.jade

and finally execute the action http://127.0.0.1:3000/example/hello.html