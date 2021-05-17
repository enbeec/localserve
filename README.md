# localserve
a script for working with serve and json-server

## Installation
Just copy the **entire** `localserve` directory (first clone the repo) into your repo. _(You can also add it as a submodule.)_ Everything else is documented within `localserve` itself. This is also where you set your configuration variables. 

Once it's customized you can run it with `localserve/localserve` assuming you installed it with the workspace set to your repository root. If you want to make a shortcut for easier access, run `ln -s localserve/localserve serve-my-project` then run localserve by doing `./serve-my-project`.

Also, it's a good idea to add the following to your `.gitignore` so you don't track transient things like logfiles and live database files:

```
api/db.json
*/json-server.log
*/serve.log