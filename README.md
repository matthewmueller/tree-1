tree
---
> An implementation of the [`tree`](http://mama.indstate.edu/users/ice/tree/) command written in Go, that can be programmatically.

#### Installation:
```sh
$ go get github.com/a8m/tree
```

#### How to use `tree` programmatically ?
You can take a look on `cmd/tree`, and [s3tree](http://github.com/a8m/s3tree) or see the example below.
```go
import (
    "github.com/a8m/tree"
)

func main() {
    opts := &tree.Options{
        // Fs, and OutFile are required fields.
        // Fs should implement the tree file-system interface(see: tree.Fs),
        // and OutFile should be type io.Writer
        Fs: fs,
        OutFile: os.Stdout,
        // ...
    }
    inf.New("root-dir")
    // Visit all nodes recursively
    inf.Visit(opts)
    // Print nodes 
    inf.Print(opts)
}
```

### License
MIT
