# Pattern: [Trick / Pattern Name]

## 🧠 Core Concept
(One sentence explaining how the trick works. e.g., "Maintain a window that expands to the right to include elements, and shrinks from the left when a condition is broken.")

## 🎯 When to Use (Triggers)
- Keyword 1 (e.g., "Subarray", "Substring")
- Keyword 2 (e.g., "Contiguous elements", "Longest/Shortest/Max/Min")
- Constraint (e.g., "Must be O(N) time")

## 🏗️ The Skeleton Code
```python
# The universal template you can memorize and adapt
def pattern_template(nums):
    # Initialize variables

    for right in range(len(nums)):
        # Add nums[right] to current state

        while (condition_broken):
            # Remove nums[left] from state
            # left += 1

        # Update answer
```

## 🔄 Common Variations
1. **[Variation Name]:** (e.g., "Fixed Size Window") - (How the template changes: "Remove the `while` loop, just check if `right - left + 1 == k`")
2. **[Variation Name]:** (e.g., "Dynamic Window") - (How the template changes: "Use the `while` loop to shrink until valid")
