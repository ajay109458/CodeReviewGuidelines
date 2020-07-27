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

## Sources
- https://nyu-cds.github.io/effective-code-reviews/03-checklist/
- https://github.com/ahammel/code-review-checklist/blob/master/code-review-checklist.md
- https://github.com/joho/awesome-code-review
- https://medium.com/@same7mabrouk/the-checklist-of-my-code-review-18cc6f6fb5b3
- https://levelup.gitconnected.com/you-need-a-code-review-checklist-1524e6a2d2cd
- 
