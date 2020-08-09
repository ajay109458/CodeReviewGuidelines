### Package Naming
- Package name shouldn't have underscore, hyphen or mixedCaps
- Packages shouldn't be named with generic naming schemes, such as common, util, base or helper.
- Package name should be related to the function that the package is performing.
- Package should have a decent scope, all the elements in a package should have a similar scope. 

#### Package structure
```
exampleProgram
-cmd
  - cli
    - main.go
  - web
    - main.go
- Dockerfile
- go.mod
- go.sum
- pkg
  - api
  - integration
  - notification
```

### Go module
Create a go module with command 
```
go mod init repository
```

### Understanding naming in Go

There are lot of consistent behaviors that Go programmers like to retain in order to keep readable, maintainable code. 

##### Local Variables shoudl be small and crisp
- `i` for iterator
- `r` for reader
- `w` for writer
- `ch` for channel

##### Global variables should be short and descriptive
- RateLimit
- Log
- Pool

##### Acronyms should follow the convention of using all capitals
- FooJSON
- FooHTTP

##### Avoid stuttering with the package name:
- log.Error() instead of log.LogError()

##### Interface with one method should follow the method name plus `er` suffix
- Stringer
- Reader
- Writer
- Logger

##### Names in Go should follow a Pascal or mixedCaps case method:
- var ThingOne
- var thingTwo
