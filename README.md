# golang-dcvs-embed-id
Embed DCVS id into go binary

```
> cat main.go
package main

import "fmt"

var x string

func main() {
           fmt.Println(x)
}
> git rev-parse --short HEAD
876e7fd
> go build -ldflags="-X main.x=$(git rev-parse --short HEAD)" main.go
> ./main
876e7fd
```
