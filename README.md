### Go + Instgaram API
<p align="center"><img width=100% src="https://raw.githubusercontent.com/ahmdrz/goinsta/v1/resources/goinsta-image.png"></p>

> Unofficial Instagram API for Golang

[![GoDoc](https://godoc.org/github.com/ahmdrz/goinsta?status.svg)](https://godoc.org/github.com/ahmdrz/goinsta) [![Go Report Card](https://goreportcard.com/badge/github.com/ahmdrz/goinsta)](https://goreportcard.com/report/github.com/ahmdrz/goinsta)

### Features

* **HTTP2 by default. Goinsta uses HTTP2 client enhancing performance.**
* **Object independency. Can handle multiple instagram accounts.**
* **Like Instagram mobile application**. Goinsta is very similar to Instagram official application.
* **Simple**. Goinsta is made by lazy programmers!
* **Backup methods**. You can use `Export` and `Import` functions.
* **Security**. Your password is only required to login. After login your password is deleted.

### Package installation 

`go get -u -v gopkg.in/ahmdrz/goinsta.v2`

### CLI installation

```
go get -u -v gopkg.in/ahmdrz/goinsta.v2
go install gopkg.in/ahmdrz/goinsta.v2/goinsta
```

### Example

```go
package main

import (
	"fmt"

	"gopkg.in/ahmdrz/goinsta.v2"
)

func main() {
  //insta, err := goinsta.Import("~/.goinsta")
  insta := goinsta.New("USERNAME", "PASSWORD")

  // also you can use New function from gopkg.in/ahmdrz/goinsta.v2/utils

  // insta.SetProxy("http://localhost:8080", true) // true for insecure connections
  if err := insta.Login(); err != nil {
    fmt.Println(err)
    return
  }
  // export your configuration
  // after exporting you can use Import function instead of New function.
  insta.Export("~/.goinsta")

  ...
}
```

* [**More Examples**](https://github.com/ahmdrz/goinsta/tree/master/examples)

### Projects using `goinsta`

- [instagraph](https://github.com/ahmdrz/instagraph)
- [icrawler](https://github.com/themester/icrawler)
- [go-instabot](https://github.com/tducasse/go-instabot)
- [ermes](https://github.com/borteo/ermes)
- [nick\_bot](https://github.com/icholy/nick_bot)
- [goinstadownload](https://github.com/alejoloaiza/goinstadownload)
- [instafeed](https://github.com/falzm/instafeed)
- [keepig](https://github.com/seankhliao/keepig)
- ...

### Legal

This code is in no way affiliated with, authorized, maintained, sponsored or endorsed by Instagram or any of its affiliates or subsidiaries. This is an independent and unofficial API. Use at your own risk.

### Versioning

Goinsta used gopkg.in as versioning control. Stable new API is the version v2.0. You can get it using:
```bash
go get -u -v gopkg.in/ahmdrz/goinsta.v2
```

### Donate

**Ahmdrz**

![btc](https://raw.githubusercontent.com/reek/anti-adblock-killer/gh-pages/images/bitcoin.png) Bitcoin: `1KjcfrBPJtM4MfBSGTqpC6RcoEW1KBh15X`

**Mester**

![btc](https://raw.githubusercontent.com/reek/anti-adblock-killer/gh-pages/images/bitcoin.png) Bitcoin: `37aogDJYBFkdSJTWG7TgcpgNweGHPCy1Ks`


[![Analytics](https://ga-beacon.appspot.com/UA-107698067-1/readme-page)](https://github.com/igrigorik/ga-beacon)

