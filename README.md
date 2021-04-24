# Terraform Provider Algolia
![License: MIT](https://img.shields.io/badge/License-MPL2.0-blue.svg)
![Test Workflow](https://github.com/k-yomo/terraform-provider-algolia/workflows/Tests/badge.svg)
[![codecov](https://codecov.io/gh/k-yomo/terraform-provider-algolia/branch/main/graph/badge.svg)](https://codecov.io/gh/k-yomo/terraform-provider-algolia)
[![Go Report Card](https://goreportcard.com/badge/k-yomo/terraform-provider-algolia)](https://goreportcard.com/report/k-yomo/terraform-provider-algolia)

Fully tested Terraform Provider for Algolia.

## Requirements

-	[Terraform](https://www.terraform.io/downloads.html) >= 0.13.x
-	[Go](https://golang.org/doc/install) >= 1.15

## Building The Provider

1. Clone the repository
1. Enter the repository directory
1. Build the provider using the Go `install` command: 
```sh
$ go install
```

## Adding Dependencies

This provider uses [Go modules](https://github.com/golang/go/wiki/Modules).
Please see the Go documentation for the most up to date information about using Go modules.

To add a new dependency `github.com/author/dependency` to your Terraform provider:

```
go get github.com/author/dependency
go mod tidy
```

Then commit the changes to `go.mod` and `go.sum`.

## Using the provider

Fill this in for each provider

## Developing the Provider

If you wish to work on the provider, you'll first need [Go](http://www.golang.org) installed on your machine (see [Requirements](#requirements) above).

To generate or update documentation, run `make generate`.

### Test
Set required env variables.
```
$ echo ALGOLIA_APP_ID={APP_ID} >> .env
$ echo ALGOLIA_API_KEY={API_KEY} >> .env
$ direnv allow
```

Run `make testacc` to run the full suite of Acceptance tests.
```sh
$ make testacc
```
*Note:* Acceptance tests create real resources, and often cost money to run.

