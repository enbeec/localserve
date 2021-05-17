# localserve
a script for working with serve and json-server

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
