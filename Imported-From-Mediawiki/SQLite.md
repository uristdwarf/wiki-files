---
title: SQLite
description: 
published: true
date: 2022-08-07T13:50:44.267Z
tags: 
editor: markdown
dateCreated: 2022-08-04T16:21:53.224Z
---

# SQLite
SQLite is a embedded [SQL](SQL "wikilink") database management system.

## SQLite in Go {#sqlite_in_go}

To use it in Go, you need to import a \"driver\" for it. There are
[various](https://github.com/golang/go/wiki/SQLDrivers) SQLite drivers
available, but the recommended (and the one projects require you to use)
is *[go-sqlite3](https://github.com/mattn/go-sqlite3).*

To import it, add to your import list in main.go:

``` go
import (
    // All your other packages

    _ "github.com/mattn/go-sqlite3"
)
```

And that's it! To actually interact with the database, you need to use
the [database/sql](Go_standard_library/database "wikilink") package.
