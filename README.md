# Online Futhark REPL
This is a website that can start Futhark REPL processes and let users interact with the REPLs through a website.

To start the website in debugging mode do.
```
cd repl && flask --app app run --debug
```
or just use `flask run`.
```
cd repl && flask run
```

## Settings
Inside [repl/settings.json](repl/settings.json) are some paramaters which have the following meanings:

* `check_time`: How often the webserver should check if there are sessions to clean up (in minutes). 
* `last_time_limit`: The amount of time an REPL session can be inactive before it is cleaned (in minutes).
* `token_lifespan`: The amount of time a tokens can exists before it becomes invalid (in minutes).
* `response_size_limit`: The maximum reponse size, the website can give to a user (in bytes).
* `compute_time_limit`: The maximum amount of time a computation may take (in seconds).
* `session_amount_limit`: The maximum amount of active sessions, null the amount is unlimited.

## TODO
* Add a way of deploying the website.
* The project should be contained within a docker file.
* Documentation.