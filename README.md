{{package_name}}
==================

{{package_description}}

It is built on top of Express.js which runs on Node.js.

It reads the {{package_rest_api_module_name}} module, and provides a simple express server,
which echoes the mock data defined under the services.

You can modify and extend this code as you like to fit your needs.
The `api.js` contains the implementation functions of the REST API calls which are referred from 
the `service.yml` descriptor files.


## Prerequisites

In order to run the server, you need to have the Node.js and npm installed on your machine.


## Installation

Clone the [{{package_github_account}}/{{package_name}}](https://github.com/{{package_github_account}}/{{package_name}}) server into a folder:

    clone git@github.com:{{package_github_account}}/{{package_name}}.git

Install the required dependencies:

    cd {{package_name}}
    npm install


## Usage

### Start the server

To start the server, execute the following command in the `server` folder:

Start the mock server:

    node server/server.js

    register service GET /monitoring/isAlive
    /monitoring/isAlive
    register service GET /rtc
    /rtc
    ...

    Express server listening on port 3007 in development mode

Check if the server is properly working via executing the following command 
in a separate console or opening the link with a browser:

    $ curl http://localhost:3007/rest/monitoring/isAlive
    true


### Server configuration

The `server/config.yml` file contains the configuration parameters for the server.

You can define many parameters, including:

- The folder of the web content for the UI
- The proxy for the final version of implemented backend services
- etc.

You can group these setting into so called modes, that you can select when you start the server.
To change the configuration, edit this `server/config.yml` file, and restart the server.

You also can add mock implementation logic,
in case the built-in and dumb mock data responses are not enough for testing and frontend development.
You can find example for this in the `server/monitoring.js` file.

To learn more about the server and its configuration, or how to extend the mock functionality 
with custom code visit the [rest-tool homepage](http://tombenke.github.io/rest-tool/) of the project, or
go directly to the [mock server documentation](http://tombenke.github.io/rest-tool/docs/server.html) pages.


## todos

- Add test
    - Test each endpoint/method/testCase.

## References

- [{{package_name}}](https://github.com/{{package_github_account}}/{{package_name}})
- [rest-tool homepage](http://tombenke.github.io/rest-tool/)
- [rest-tool / mock server documentation](http://tombenke.github.io/rest-tool/docs/server.html)
