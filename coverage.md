# Control Flow Coverage

What we changed:
- Range Test:
    UNKNOWN
    - testUpperBound_FailsWhenLessThanLowerBound()
    - testUpperBound_FailsWhenLessThanLowerBound_BVT_BLB()
    - testGetLength_PositiveLength() (fixed typo lol)
    FINALIZED
    - testUpperBound_FailsWhenLessThanLowerBound
    - testUpperBound_FailsWhenLessThanLowerBound_BVT_BLB
    - testGetLength_PositiveLength

- DataUtilities Test:
    UNKNOWN
    - calculateRowTotal_CorrectTotal
    - testGetCumulativePercentages_WithVerySmallValues
    - testCalculateColumnTotal_NegativeColumnArg_BLB
    - testGetCumulativePercentages_WithVerySmallValues
    FINALIZED
    - testCalculateColumnTotal_UsingNullAsDataArgument
    - testCalculateColumnTotal_NegativeColumnArg_BLB
    - testGetCumulativePercentages_NullDataArg
    - testGetCumulativePercentages_WithAllNulls
    - testGetCumulativePercentages_WithVerySmallValues
    - calculateRowTotal_CorrectTotal
    - calculateRowTotalWithNegativeValues_ReturnCorrectTotal
    - calculateRowTotalWithZeroValues_ReturnCorrectTotal
    - calculateRowTotalWithEmptyDataSet_ReturnZeroTotal
    - testCreateNumberArray2D_ValidArray
    - testCreateNumberArray2D_NullArray



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



---

# Data Flow Coverage

DataUtilities.calculateColumnTotal
Range.contains

for each test case, show which pairs are covered

| Test Case | DU-Pairs Covered |
|-----------|------------------|
|testCalculateColumnTotal_UsingNullAsDataArgument| data: { (123, 124) }                  |
|testCalculateColumnTotal_ZeroRows| data: { (123, 124), (123, 126) }, <br/> rowCount: { (126, 127), (126, 133) }, <br/> r: { (127, 127) }, r2: { (133, 133) } |
|testCalculateColumnTotal_ZeroColumns| data: { (123, 124), (123, 126) (123, 128), (123, 134) },<br/> rowCount: { (126, 127), (126, 133) }, <br/> r: { (127, 127), (127, 128) }, <br/> r2: { (133, 133), (133, 134) }, <br/> column: { (123, 128), (123, 134) }, <br/> n: { (128, 129), (134, 135) }                  |
|testCalculateColumnTotal_NegativeColumnArg_BLB| data: { (123, 124), (123, 126) (123, 128) }, <br/> rowCount: { (126, 127) }, <br/> r: { (127, 127), (127, 128) }, <br/> column: { (123, 128) }                 |
|testCalculateColumnTotal_ColumnEqualsZero_LB| data: { (123, 124), (123, 126), (123, 128), (123, 134) }, <br/> rowCount: { (126, 127), (126, 133) }, <br/> r: { (127, 127), (127, 128) }, <br/> r2: { (133, 133), (133, 134) }, <br/> column: { (123, 128), (123, 134) }, <br/> n: { (128, 129), (128, 130), (134, 135), (134, 136) }, <br/> total: { (125, 130), (130, 130), (130, 136), (136, 136) } |
|testCalculateColumnTotal_ColumnIsNominal| data: { (123, 124), (123, 126), (123, 128), (123, 134) }, <br/> rowCount: { (126, 127), (126, 133) }, <br/> r: { (127, 127), (127, 128) }, <br/> r2: { (133, 133), (133, 134) }, <br/> column: { (123, 128), (123, 134) }, <br/> n: { (128, 129), (128, 130), (134, 135), (134, 136) }, <br/> total: { (125, 130), (130, 130), (130, 136), (136, 136) }  |
|testCalculateColumnTotal_ColumnIsAtUB| data: { (123, 124), (123, 126) (123, 128), (123, 134) },<br/> rowCount: { (126, 127), (126, 133) }, <br/> r: { (127, 127), (127, 128) }, <br/> r2: { (133, 133), (133, 134) }, <br/> column: { (123, 128), (123, 134) }, <br/> n: { (128, 129), (134, 135) } |
|testCalculateColumnTotal_ColumnIsAUB| data: { (123, 124), (123, 126) (123, 128), (123, 134) },<br/> rowCount: { (126, 127), (126, 133) }, <br/> r: { (127, 127), (127, 128) }, <br/> r2: { (133, 133), (133, 134) }, <br/> column: { (123, 128), (123, 134) }, <br/> n: { (128, 129), (134, 135) } |
|testContains_ValueInRange|value: { (158, 159), (158, 162), (158, 165) } |
|testContains_ValueNotInRange|value: { (158, 159), (158, 162) }|
|testContains_LowerBound|value: { (158, 159), (158, 162), (158, 165) }|
|testContains_UpperBound|value: { (158, 159), (158, 162), (158, 165) }|
|testContains_NullRange|value: { (158, 159), (158, 162) }|

**Range.contains DU-pair Coverage = 3 / 3 = 100%** <br/>
**DataUtilities.calculateColumnTotal DU-pair Coverage = 20 / 20 = 100%**