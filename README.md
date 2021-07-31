<h2 align="center">Simple HTML Modification in Go</h2>
Do you grin at the sight of html.Node ? Me too.

Modifying HTML in Go should be simple.


**🧘🏻 Human friendly**: query language for humans that takes a minute to grasp.

**🎓 Simplicity**: no robust solution here just one single goal

## Getting Started

```go
package main
import "github.com/asaf-shitrit/html-overwrite"

func main(){

    // load
    doc := html_overwrite.Load(`
       <html>
            <body>
                <h1 id="content">Hello !</h1>
            </body>
       </html>
    `)

    // mutate
    doc.Set("id=content", "Bye Bye")

    // get back
    newStringDoc := doc.String()
}
```

## State
- Will be actively developed by me based on features I require in personal projects
- Tests will be added to each new feature release 
- CI will be integrated in future release
- Feel free to create new issues if you find any 😃
