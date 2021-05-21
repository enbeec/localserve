# localserve
a script for working with serve and json-server

![an example of localserve from my daily journal project](https://vcvcvc-dev.us-east-1.linodeobjects.com/localserve.gif)

Here's what it does:

- asks you if you want to re-initialize your database
- runs json-server for you using the `--watch` flag
- runs serve for you
- reminds you of the port numbers you picked
- when you press `ctrl+c` it cleans everything up!

## Installation

### Prepare your project
Let's say your project is called "my-project", has website source code at `my-project/src` and contains a database file `my-project/api/db.json`. Get your database set up just how you like it for testing and then copy that file to back up the initial state of your database. This way, `localserve` can ask you if you want to re-initialize your data every time you serve!

Here's what that might look like in the terminal:
```shell
$ cd workspace/my-project
## ... set up your database ...
$ cp api/db.json api/db.json.init
# fun version: cp api/db.json{,.init}
```

### Install the script
Clone this repo and run `./install-localserve my_project_dir`.
Edit the newly created 'my-localserve' file and set the variables for your project's name (or the name of the working directory) and your database files. You can also set custom port numbers here. The defaults are 8080 for serve and 8081 for json-server.

### Optional, but strongly recommended!
Also, it's a good idea to add the following to your `.gitignore` so you don't track transient things like logfiles and live database files:

```
api/db.json
*/json-server.log
*/serve.log
json-server.log
serve.log
```

You can also just copy the `.gitignore` included in the repo.

## Known Issues

Right now you can't run two localserve sites at once, but this is a pretty easy limitation to bypass. Hit me up if you want that!
