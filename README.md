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
