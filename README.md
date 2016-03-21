# most-web-jade (in progress)
Most Web Framework Jade View Engine

![MOST Web Framework Logo](https://www.themost.io/assets/images/most_logo_sw_240.png)

A view engine for jade templates which are going to be used in web applications based on [MOST Web Framework](https://github.com/kbarbounakis/most-web)

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
