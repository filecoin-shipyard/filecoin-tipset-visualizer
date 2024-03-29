# filecoin-tipset-visualizer

## Status

This repository is in a **frozen** state. It is not being maintained or kept in sync with the libraries it depends on. Even though work on this repository has been **shelved**, anyone interested in updating or maintaining this library should express their interest on one Filecoin community conversation mediums: <https://github.com/filecoin-project/community#join-the-community>.

---

> agency enterprise filecoin-explorer-lotus

## Usage

First, you need lotus up and running. Follow [these instructions](https://docs.lotu.sh/en+install-lotus-ubuntu).

Next, run the daemon, sync the chain, and run the chain watcher.

```bash
$ ./lotus daemon

# in another terminal
$ ./lotus sync wait

# in yet another terminal
$ ./chainwatch --db='postgres://postgres:@localhost:5432/lotus?sslmode=disable' run

or

$ go run ./cmd/lotus-chainwatch --db postgres://user:password@localhost:5434/lotus?sslmode=disable run

```

Finally, inside of this repo's directory, run the following commands:

```bash
# use docker-compose
$ docker-compose up

# or, use yarn / npm
$ yarn install
$ yarn start
```

## License

[LICENSE](LICENSE)

```
The MIT License (MIT)

Copyright (c) 2020 Agency Enterprise

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.
```
