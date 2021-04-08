# Golang Mux Demo

[![Build Status](https://tomfern.semaphoreci.com/badges/go-mux-api/branches/master.svg)](https://tomfern.semaphoreci.com/projects/go-mux-api)

Read the complete post with the explanation here:

https://semaphoreci.com/community/tutorials/building-and-testing-a-rest-api-in-go-with-gorilla-mux-and-postgresql

## Run locally

- Start postgres
- Prepare environment, fill DB parameters:

``` bash
$ source env-sample
```

- Build and run:

```bash
$ export GO111MODULE=on
$ export GOFLAGS=-mod=vendor
$ go mod download
$ go build -o go-mux-api.bin
$ ./go-mux-api.bin
```

Server is listening on localhost:8010

## Test

```bash
$ go test -v
=== RUN   TestEmptyTable
--- PASS: TestEmptyTable (0.00s)
=== RUN   TestGetNonExistentProduct
--- PASS: TestGetNonExistentProduct (0.00s)
=== RUN   TestCreateProduct
--- PASS: TestCreateProduct (0.00s)
=== RUN   TestGetProduct
--- PASS: TestGetProduct (0.00s)
=== RUN   TestUpdateProduct
--- PASS: TestUpdateProduct (0.01s)
=== RUN   TestDeleteProduct
--- PASS: TestDeleteProduct (0.01s)
PASS
ok      _/home/tom/r/go-mux-api 0.034s
```

## License

Copyright (c) 2021 Rendered Text

Distributed under the MIT License. See the file LICENSE.
