# go-graphalgo.github.io

The go-graphalgo landing page (Hugo), served at <https://go-graphalgo.github.io/>.
The documentation is at <https://go-graphalgo.github.io/docs/> (repository
[go-graphalgo/docs](https://github.com/go-graphalgo/docs)).

The organization is **planned (wave 3)**: it holds no library yet, and the page
says so, with what it will cover and a link to the plan in
[go-scikit/roadmap](https://github.com/go-scikit/roadmap).

The layout is the go-* family template: `layouts/index.html` and the shared
design (stylesheet, theme toggle, fork ribbon, icons), imported as the Hugo
module `github.com/go-fleettools/landingkit` pinned in `go.mod`. `[params.brand]`
in `hugo.toml` is read from the logo's gradient:

```sh
go run github.com/go-fleettools/landingkit/cmd/landingkit brand static/img/logo.svg
hugo server
```

| Workflow | What |
| --- | --- |
| `hugo.yml` | builds on pull requests; builds and deploys to Pages on `main` |
| `ci.yml` | the site builds and names every repository; `go mod tidy` keeps the landingkit requirement |
| `links.yml` | every link and image of the built site resolves |

BSD-3-Clause.
