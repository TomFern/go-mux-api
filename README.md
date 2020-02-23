# Golang Mux Demo

## Run locally

- Start postgres
- Prepare environment, fill DB parameters:

``` bash
$ cp env-sample .env
$ $EDITOR .env
$ source .env
```

- Build and run:

```bash
$ go get -u github.com/gorilla/mux github.com/lib/pq
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

The project is open-sourced software licensed under the [MIT license](https://opensource.org/licenses/MIT).
