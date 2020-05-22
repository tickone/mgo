Contributing
-------------------------

We really appreciate contributions, but they must meet the following requirements:

* A PR should have a brief description of the problem/feature being proposed
* Pull requests should target the `development` branch
* Existing tests should pass and any new code should be covered with it's own test(s) (use [travis-ci](https://travis-ci.org))
* New functions should be [documented](https://blog.golang.org/godoc-documenting-go-code) clearly
* Code should pass `golint`, `go vet` and `go fmt`

We merge PRs into `development`, which is then tested in a sharded, replicated environment in our datacenter for regressions. Once everyone is happy, we merge to master - this is to maintain a bit of quality control past the usual PR process.

**Thanks** for helping!

# How to test the code
In order to run the tests, you need the following installed (assuming Ubuntu)

* daemontools (for svstat)
* mongo (for mongo client)
* mongodb (for mongo server)

Before running the tests, you need to start the test mongo server with `make startdb`. After the tests are done, you
can tear it down with `make stopdb`.

The tests to run are defined in `.travis.yml` under the *script* section.