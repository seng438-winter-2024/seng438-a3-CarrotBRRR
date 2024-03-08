# Control Flow Coverage

What we changed:
- Range Test:
    - testUpperBound_FailsWhenLessThanLowerBound()
    - testUpperBound_FailsWhenLessThanLowerBound_BVT_BLB()
    - testGetLength_PositiveLength() (fixed typo lol)

- DataUtilities Test:
    - calculateRowTotal_CorrectTotal
    - testGetCumulativePercentages_WithVerySmallValues
    - testCalculateColumnTotal_NegativeColumnArg_BLB
    - testGetCumulativePercentages_WithVerySmallValues
Old
| Test Class            | Statement Coverage | Branch Coverage | Method Coverage    |
|-----------------------|--------------------|-----------------|--------------------|
| Range Test            | 94.8%              | No Branches     | 93.5%              |
| DataUtilities Test    | 90.1%              | 100%            | 100%               |

New
| Test Class            | Statement Coverage | Branch Coverage | Method Coverage    |
|-----------------------|--------------------|-----------------|--------------------|
| Range Test            | 96.7%              | No Branches     | 100%               |
| DataUtilities Test    | 96.4%              | 100%            | 100%               |


Note: 
- Line Coverage in EclEmma is the same as Statement Coverage
- Method Coverage: Percentage of methods that was executed during testing

# Coverage tools
Explain what you fixed (e.g., removing mock objects, updating IDEs, switching to another tool, etc.)

## eclEmma
### Pros of EclEmma: 
- Easy to use
- Built in to eclipse
- Has useful coverage metrics

### Cons EclEmma:
- No condition coverage

## Metrics:
- Statement Coverage Pros: Identifies executed code.
- Statement Coverage Cons: Doesn't guarantee logical correctness.
- Branch Coverage Pros: Identifies paths not taken.
- Branch Coverage Cons: Doesn't guarantee branch condition correctness.
- Method Coverage Pros: Ensures all methods are tested.
- Method Coverage Cons: Doesn't ensure method perform properly in all scenarios.

---

# Data Flow Coverage

DataUtilities.calculateColumnTotal
Range.contains

