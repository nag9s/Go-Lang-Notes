# Access documentation offline

To browse full documentation locally, run:

```
$ godoc -http=localhost:9000
```

Then open[localhost:9000](http://localhost:9000/)in the browser. It’ll show the same information as[https://golang.org/doc/](https://golang.org/doc/).

You can run guided tour locally with:

```
$ go get golang.org/x/tour/gotour
$ go tool tour
```

This runs[https://tour.golang.org/](https://tour.golang.org/)locally.

You can use`godoc`for quick reference. For example, to see documentation for`fmt.Print`:

```
$ godoc cmd/fmt Print
```

General help is also available from the command-line:

```
$ go 
help
[
command
]
```



