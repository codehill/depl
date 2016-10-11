# depl
Short for disposable email providers list, is a Go package for checking email addresses against a list of disposable email provider domains.

## Usage
* Download and install the package:  
```
go get github.com/codehill/depl
```
* Check a domain name and an email address:
```go
package main

import (
	"fmt"

	"github.com/codehill/depl"
)

func main() {
	if check, err := depl.IsDomainDisposable("example.com"); err == nil {
		if check {
			fmt.Println("Domain name is in depl list")
		} else {
			fmt.Println("Domain name is not in depl")
		}

	} else {
		fmt.Println(err)
	}

	if check, err := depl.IsEmailDisposable("example@example.com"); err == nil {
		if check {
			fmt.Println("Domain name is in depl list")
		} else {
			fmt.Println("Domain name is not in depl")
		}

	} else {
		fmt.Println(err)
	}
}
```

## Contributing
* If you've got any suggestions or questions, [please create an issue here](https://github.com/codehill/depl/issues).
* If you want to contribute to the list, fix a bug or implement a feature, please feel free to do so. Just send me a pull request.

## License
This project is licensed under a MIT license. See the included [LICENSE file](LICENSE) for more details.
