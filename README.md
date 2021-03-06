## feeds2imap.clj

RSS/Atom reader implemented in Clojure.
It stores new items in the mail folders using IMAP APPEND command (java.mail framework).

### Configuration
By default configuration dir is `$HOME/.config/feeds2imap.clj`.

The only file required to run the code is *imap.clj*. Take a look at *imap.clj.example* for details.

Feeds and folders can be added using the `add` command (see below), or you can write them directly in the *urls.clj* file (inside the configuration directory).
The format of this file is as follows:

```clojure
{:folder1 ["url1" "url2" ...]
 :folder2 [...]
 ...}
```

### Usage
You can use `lein run` to run programm or you can generate jar with `lein uberjar` and run programm with `java -jar <path-to-jar>`.

* `LAUNCH-COMMAND` - pull new items.
* `LAUNCH-COMMAND pull` - pull new items.
* `LAUNCH-COMMAND auto` - pull new items every 1 hour in the loop.
* `LAUNCH-COMMAND show` - show feeds list (url.clj file content).
* `LAUNCH-COMMAND add folder-name feed-url` - add url to feeds file to the folder folder-name.

where `LAUNCH-COMMAND = lein run / lein trampoline run / java -jar jarfile.jar`.

### License

Copyright © 2013 Max Gonzih gonzih at gmail.com

Distributed under the Eclipse Public License, the same as Clojure.

### Thanks
Thanks to Greg Hendershott for original idea implemented in Racket
http://www.greghendershott.com/2013/05/feeds2gmail.html

### Similar projects

* [My Ruby prototype](https://github.com/Gonzih/feeds2imap.rb)
* [My Clojure implementation](https://github.com/Gonzih/feeds2imap.clj)
* [Racket implementation](https://github.com/greghendershott/feeds2gmail)
* [Haskell implementation](https://github.com/cordawyn/rss2imap)
