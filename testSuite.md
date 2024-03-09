Range: 
- For getLength:
    - boundary: infinte boundary
        - finite to infinite
        - negative infinite to finite

DataUtilities:
- Row Total:
    - Null Last Element
- Column Total:
    - Null Last Element

What we changed:
- Range Test:
    - testUpperBound_FailsWhenLessThanLowerBound
    - testUpperBound_FailsWhenLessThanLowerBound_BVT_BLB
    - testGetLength_PositiveLength

- DataUtilities Test:
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