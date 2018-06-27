# pgweb

Web-based PostgreSQL database browser written in Go.

[![Release](https://img.shields.io/github/release/sosedoff/pgweb.svg?label=Release)](https://github.com/yrong/pgweb/releases)
[![Linux Build](https://img.shields.io/travis/sosedoff/pgweb/master.svg?label=Linux)](https://travis-ci.org/sosedoff/pgweb)
[![Windows Build](https://img.shields.io/appveyor/ci/sosedoff/pgweb/master.svg?label=Windows)](https://ci.appveyor.com/project/sosedoff/pgweb)
[![Go Report Card](https://goreportcard.com/badge/github.com/yrong/pgweb)](https://goreportcard.com/report/github.com/yrong/pgweb)
[![GoDoc](https://godoc.org/github.com/yrong/pgweb?status.svg)](https://godoc.org/github.com/yrong/pgweb)

## Overview

Pgweb is a web-based database browser for PostgreSQL, written in Go and works
on OSX, Linux and Windows machines. Main idea behind using Go for backend development
is to utilize ability of the compiler to produce zero-dependency binaries for 
multiple platforms. Pgweb was created as an attempt to build very simple and portable
application to work with local or remote PostgreSQL databases.

[See application screenshots](SCREENS.md)

## Features

- Cross-platform support OSX/Linux/Windows 32/64-bit
- Simple installation (distributed as a single binary)
- Zero dependencies
- Works with PostgreSQL 9.1+
- SSH Connections
- Multiple database sessions
- Simple database browser
- Execute and analyze custom SQL queries
- Table and query data export to CSV/JSON/XML
- Query history
- Server bookmarks

Visit [WIKI](https://github.com/yrong/pgweb/wiki) for more details

## Demo

Visit https://pgweb-demo.herokuapp.com to see pgweb in action.

## Installation

[Precompiled binaries](https://github.com/yrong/pgweb/releases) for supported
operating systems are available.

[More installation options](https://github.com/yrong/pgweb/wiki/Installation)

## Usage

Start server:

```
pgweb
```

You can also provide connection flags:

```
pgweb --host localhost --user myuser --db mydb
```

Connection URL scheme is also supported:

```
pgweb --url postgres://user:password@host:port/database?sslmode=[mode]
```

### Multiple database sessions

To enable multiple database sessions in pgweb, start the server with:

```
pgweb --sessions
```

Or set environment variable:

```
SESSIONS=1 pgweb
```

## Deploy on Heroku

[![Heroku Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy?template=https://github.com/yrong/pgweb)

## Testing

Before running tests, make sure you have PostgreSQL server running on `localhost:5432`
interface. Also, you must have `postgres` user that could create new databases
in your local environment. Pgweb server should not be running at the same time.

Execute test suite:

```
make test
```

If you're using Docker locally, you might also run pgweb test suite against
all supported PostgreSQL version with a single command:

```
make test-all
```

## Contribute

- Fork this repository
- Create a new feature branch for a new functionality or bugfix
- Commit your changes
- Execute test suite
- Push your code and open a new pull request
- Use [issues](https://github.com/yrong/pgweb/issues) for any questions
- Check [wiki](https://github.com/yrong/pgweb/wiki) for extra documentation

## Premium Features

If you or your company would like to sponsor a custom feature, please let me know
via email (see contact section). Custom features are developed exclusively for the
client and not committed to the public repo. 

## Donations

Pgweb is free and open source software, there's no plan to make a business out of it.
If you wish to support the development, you can send a donation of any size using
the following platforms:

- Paypal: dan.sosedoff@gmail.com
- Bitcoin: 1qAGohEhuNEkJEhHyEQfLgXAwY7dWRhmU

Any contribution is much appreciated. 

## Contact

- Ronyang
- [yrong1997@gmail.com]

## License

The MIT License (MIT). See [LICENSE](LICENSE) file for more details.

Copyright (c) 2014-2018 Ronyang, <yrong1997@gmail.com>