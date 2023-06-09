# ssw-go-jwt
<hr>

A **S**tupid **S**imple **W**rapper for [golang-jwt](https://github.com/golang-jwt/jwt).

## Supported Algorithms
Currently, only the RS256 and HS256 signing algorithm is supported.

## Usage
You can use this library in two different modes, validation-only mode or full mode. To use full mode, simply specify both private and public key files paths. To use validation-only mode, just specify the public key files paths.

## Installation
```shell
go get github.com/RaymondSalim/ssw-go-jwt
```

## Code Example
```go
package example

import "github.com/RaymondSalim/ssw-go-jwt"

func example() {
	// Start by initializing the NewGoJWT interface
	ssw := NewGoJWT{
		config: JWTConfig{
			...
		}
	}
	
	// Make sure to call Init() before running any other functions
	err := ssw.Init()
	
	// Use methods as you'd like
	t, err := ssw.GenerateTokens(...)
	err = ssw.ValidateToken(...)
	err = ssw.ValidateAccessTokenWithClaims(...)
	t, err = ssw.RenewToken(...)
}
```

## Errors
Errors returned by each function are explained in godoc

## Roadmap
- [ ] Create Example HTTP Usage File
- [ ] Update README to be more descriptive
- [ ] Add more algorithm support