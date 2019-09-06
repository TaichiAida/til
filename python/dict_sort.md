# Sorting dictionary

use **lambda**

sort key
```
scores = {"math": 70, "science": 90, "music": 80}

scores_sorted = sorted(scores.items(), key=lambda x:x[0])

print(scores_sorted)

# Output [("math", 70), ("music", 80), ("science", 90)]
```

sort value
```
scores = {"math": 70, "science": 90, "music": 80}

scores_sorted = sorted(scores.items(), key=lambda x:x[1])

print(scores_sorted)

# Output [("science", 90), ("music", 80), ("math", 70)]
```

**Caution!** the type of scores_corted is "list"
