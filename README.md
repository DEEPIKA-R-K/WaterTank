# Water Tank Problem

A frontend web app built with **Vanilla JavaScript, HTML, and CSS** that calculates how many units of water can be stored between blocks, and shows the result as an SVG diagram.

## Problem

Given an array of non-negative integers where each number is the height of a block, compute the units of water trapped between the blocks.

**Example**

Input: `[0,4,0,0,0,6,0,6,4,0]`
Output: `18 Units`

## Features

- Enter block heights as comma-separated numbers
- Calculates the total units of water stored
- Draws the tank as an SVG grid:
  - Yellow = blocks
  - Blue = water
- Validates input and shows an error for invalid values

## How to Run

1. Clone the repository:
   ```bash
   git clone <your-repo-url>
   ```
2. Open the folder and double-click `index.html`, or open it with VS Code Live Server.

No installation or build step is needed.

## Approach

For each column, the water above it is:

```
water[i] = min(leftMax[i], rightMax[i]) - height[i]
```

- `leftMax[i]` is the tallest block from the left up to index `i`
- `rightMax[i]` is the tallest block from the right up to index `i`
- The total is the sum of the water on all columns

**Complexity:** O(n) time, O(n) space

## Sample Inputs

| Input | Output |
| `0,4,0,0,0,6,0,6,4,0` | 18 Units |
| `3,0,2,0,4` | 7 Units |
| `0,0,0` | 0 Units |

## Tech Stack

- HTML
- CSS
- Vanilla JavaScript 
