# go-labas

[![Go Reference](https://pkg.go.dev/badge/github.com/sewiti/go-labas.svg)](https://pkg.go.dev/github.com/sewiti/go-labas)
[![Build](https://github.com/sewiti/go-labas/actions/workflows/build.yml/badge.svg)](https://github.com/sewiti/go-labas/actions/workflows/build.yml)

A simple package that let's you send SMS messages using [LT Labas](https://www.labas.lt/)
mobile carrier's website.

*You need to have an active LT Labas number registered on their website at
[mano.labas.lt](https://mano.labas.lt).*

## Install

```sh
go get -u github.com/sewiti/go-labas
```

## Example

```go
package main

import labas "github.com/sewiti/go-labas"

func main() {
    cl := labas.NewClient("+37000000000", "password")

    if err := cl.SendSMS("+37000000000", "Hello World!"); err != nil {
        log.Println(err)
    }
}
```