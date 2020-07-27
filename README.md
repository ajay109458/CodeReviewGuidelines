# CodeReviewGuidelines

#### DRY (Don't repeat yourself)

Example
```
// let's assume we have a boolean and it's initialised with false
let isPositionCorrect = false
if isPositionCorrect {
    updateUI("Position Correct", isPositionCorrect)
} else {
    updateUI("Position InCorrect", isPositionCorrect)
}
```

Fix
```
let message = isPositionCorrect ? "Position Correct" : "Position InCorrect"
updateUI(message, isPositionCorrect)
```

#### Returning boolean

Example
```
func isItemExist(x: Int, items: [Int]) -> Bool {
    if items.contains(x) {
        return true
    }
    else {
        return false
    }
}
```

Fix 
```
func isItemExist(x: Int, items: [Int]) -> Bool {
    return items.contains(x)
}
```
