# HW-06b: Triangle Classification Testing Assignment

---

## 1. Assignment Description

The objective of this assignment is to:
- (a) Develop a set of test cases for an existing triangle classification program
- (b) Use those test cases to find and fix defects in that program
- (c) Report on testing results for the Triangle problem

Sometimes you will be given a program that someone else has written, and you will be asked to fix, update and enhance that program. In this assignment, you are given an existing implementation of the classify triangle program. You are also given a starter test program that tests the classify triangle program, but those tests are not complete.

The assignment consists of three parts:

**Part 0:** Create a GitHub repository named "hw-06b" and commit the original Triangle.py and TestTriangle.py files in their original form.

**Part 1:**
- Review the Triangle.py file
- Enhance the test cases in TestTriangle.py to adequately test the classify_triangle() function
- Run tests against the original implementation
- Create a formal test report (Test Report 1)
- Commit and push changes to GitHub

**Part 2:**
- Based on test results and code inspection, update Triangle.py to fix any defects found
- Run the same test set on the improved implementation
- Create a formal test report (Test Report 2)
- Commit and push changes to GitHub

---

## 2. Author

Samruddhi Sonare
SSW 567 - Software Testing, Quality Assurance and Maintenance
Stevens Institute of Technology

---

## 3. Summary

### Results Summary

**Part 0 - Repository Setup:**
- Created GitHub repository "hw-06b"
- Committed original Triangle.py with classify_triangle function
- Committed original TestTriangle.py with 6 basic tests

**Part 1 - Test Suite Enhancement:**
- Expanded test suite from 6 to 35 comprehensive test cases
- Applied systematic testing techniques (equivalence partitioning, boundary value analysis)
- Executed all 35 tests against original Triangle.py
- **Result:** 35/35 tests PASSED (100% pass rate)
- **Defects Found:** 0 functional defects

**Part 2 - Code Inspection and Improvement:**
- Performed line-by-line code inspection
- Identified 1 code quality issue (file writing at module level)
- Fixed the code organization issue
- Re-executed all 35 tests
- **Result:** 35/35 tests PASSED (100% pass rate)
- **Regressions:** None

### Reflection

**What I learned:**

1. **Systematic Testing is Essential:** Using equivalence partitioning and boundary value analysis helped organize test cases logically and identify edge cases that might otherwise be missed.

2. **Test Design Requires Planning:** Expanding from 6 basic tests to 35 comprehensive tests required careful planning. Each test case was designed with a specific purpose and grouped by category.

3. **Code Inspection Complements Testing:** Even though all tests passed, code inspection still found an improvement opportunity. Manual review can identify code quality issues that tests don't catch.

4. **Triangle Classification Complexity:** A seemingly simple problem has many edge cases including right triangle detection with floating-point tolerance, parameter order independence, and triangle inequality validation.

5. **Testing Strategy Matters:** Comprehensive coverage doesn't mean testing every possible input. Strategic selection of representative test cases from each equivalence class is more effective.

**What worked:**

- Structured approach with clear milestones (Part 0, 1, 2)
- Test organization into logical categories
- Comprehensive coverage with 35 well-designed tests
- Detailed test reports providing evidence of thoroughness
- Regular git commits creating clear project history

**What didn't work / Challenges:**

- Expected to find bugs in the original implementation but found none
- Determining test sufficiency - "did I test enough?" requires judgment
- Distinguishing between functional defects and code quality issues

**Surprises:**

- The original implementation was actually correct
- Floating-point tolerance handling in right triangle detection was well-implemented
- The code handled parameter order independence elegantly

---

## 4. Honor Pledge

"I pledge my honor that I have abided by the Stevens Honor System."

---

## 5. Detailed Results

### 1. Test Report - Running Tests Against Original Implementation

**Test Run Date:** October 24, 2025
**System Under Test:** Triangle.py (Original Implementation)
**Test Suite:** TestTriangle.py (35 comprehensive test cases)

| Test ID | Input | Expected Results | Actual Result | Pass or Fail |
|---------|-------|------------------|---------------|--------------|
| 1 | (1, 1, 1) | Equilateral | Equilateral | PASS |
| 2 | (5, 5, 5) | Equilateral | Equilateral | PASS |
| 3 | (100, 100, 100) | Equilateral | Equilateral | PASS |
| 4 | (5, 5, 3) | Isosceles | Isosceles | PASS |
| 5 | (3, 5, 5) | Isosceles | Isosceles | PASS |
| 6 | (5, 3, 5) | Isosceles | Isosceles | PASS |
| 7 | (10, 10, 15) | Isosceles | Isosceles | PASS |
| 8 | (2, 3, 4) | Scalene | Scalene | PASS |
| 9 | (5, 7, 9) | Scalene | Scalene | PASS |
| 10 | (13, 15, 20) | Scalene | Scalene | PASS |
| 11 | (3, 4, 5) | Scalene Right | Scalene Right | PASS |
| 12 | (5, 4, 3) | Scalene Right | Scalene Right | PASS |
| 13 | (5, 12, 13) | Scalene Right | Scalene Right | PASS |
| 14 | (8, 15, 17) | Scalene Right | Scalene Right | PASS |
| 15 | (1, 1, 1.414...) | Isosceles Right | Isosceles Right | PASS |
| 16 | (5, 5, 7.071...) | Isosceles Right | Isosceles Right | PASS |
| 17 | (1, 2, 3) | Not a triangle | Not a triangle | PASS |
| 18 | (1, 2, 10) | Not a triangle | Not a triangle | PASS |
| 19 | (1, 1, 5) | Not a triangle | Not a triangle | PASS |
| 20 | (10, 1, 1) | Not a triangle | Not a triangle | PASS |
| 21 | (0, 5, 5) | Not a triangle | Not a triangle | PASS |
| 22 | (5, 0, 5) | Not a triangle | Not a triangle | PASS |
| 23 | (5, 5, 0) | Not a triangle | Not a triangle | PASS |
| 24 | (0, 0, 0) | Not a triangle | Not a triangle | PASS |
| 25 | (-1, 5, 5) | Not a triangle | Not a triangle | PASS |
| 26 | (5, -1, 5) | Not a triangle | Not a triangle | PASS |
| 27 | (5, 5, -1) | Not a triangle | Not a triangle | PASS |
| 28 | (-1, -1, -1) | Not a triangle | Not a triangle | PASS |
| 29 | (1, 1, 1) | Equilateral | Equilateral | PASS |
| 30 | (100, 150, 200) | Scalene | Scalene | PASS |
| 31 | (2, 3, 4) | Scalene | Scalene | PASS |
| 32 | (2.5, 3.5, 4.5) | Scalene | Scalene | PASS |
| 33 | (2.5, 2.5, 2.5) | Equilateral | Equilateral | PASS |
| 34 | (5, 5, 5.1) | Isosceles | Isosceles | PASS |
| 35 | (10, 10, 1) | Isosceles | Isosceles | PASS |

**Test Summary:**
- Tests Planned: 35
- Tests Executed: 35
- Tests Passed: 35
- Tests Failed: 0
- Defects Found: 0
- Pass Rate: 100%

**Analysis:** The original classify_triangle() function demonstrated correct behavior across all test categories. No functional defects were identified. The function correctly classifies triangle types, detects right triangles with appropriate floating-point tolerance, and properly validates invalid inputs.

---

### 2. Source Code - Improved Triangle.py

The improved Triangle.py file is included in the repository. Key function:

```python
def classify_triangle(a, b, c):
    """
    Classifies a triangle based on side lengths.
    Returns: Equilateral, Isosceles, Scalene, adds 'Right' if applicable,
    or 'Not a triangle' if invalid.
    """
    # Validate triangle
    if a <= 0 or b <= 0 or c <= 0:
        return "Not a triangle"
    if a + b <= c or a + c <= b or b + c <= a:
        return "Not a triangle"

    # Determine type
    if a == b == c:
        triangle_type = "Equilateral"
    elif a == b or b == c or a == c:
        triangle_type = "Isosceles"
    else:
        triangle_type = "Scalene"

    # Check for right triangle
    sides = sorted([a, b, c])
    if abs(sides[0]**2 + sides[1]**2 - sides[2]**2) < 1e-6:
        triangle_type += " Right"

    return triangle_type
```

**Code Quality Improvement Made:** Moved file output code from module level into `if __name__ == "__main__":` block to prevent side effects when module is imported.

---

### 3. Source Code - Test Suite (TestTriangle.py)

The enhanced TestTriangle.py file contains 35 comprehensive test cases organized into 9 logical groups:

1. **Equilateral Triangles (3 tests):** Small, medium, and large values
2. **Isosceles Triangles (6 tests):** All pair combinations and edge cases
3. **Scalene Triangles (3 tests):** Various sizes
4. **Right Triangles (6 tests):** Pythagorean triples and different orders
5. **Invalid - Triangle Inequality (4 tests):** Violation cases
6. **Invalid - Zero/Negative (8 tests):** All positions tested
7. **Boundary Values (3 tests):** Minimum and maximum practical values
8. **Floating Point (2 tests):** Decimal value handling
9. **Edge Cases (2 tests):** Almost equilateral, very thin triangles

Complete test file is available in the repository.

---

### 4. Test Output - Running Test Suite on Improved Implementation

**Test Execution Output (test_run2_output.txt):**

```
Ran 35 tests in 0.008s

OK

Tests run: 35
Failures: 0
Errors: 0
Success rate: 100.0%
```

All 35 tests passed successfully against the improved implementation with no regressions.

---

### 5. Test Report - Running Tests Against Improved Implementation

**Test Run Date:** October 24, 2025
**System Under Test:** Triangle.py (Improved Implementation)
**Test Suite:** TestTriangle.py (35 comprehensive test cases)

| Test ID | Input | Expected Results | Actual Result | Pass or Fail |
|---------|-------|------------------|---------------|--------------|
| 1 | (1, 1, 1) | Equilateral | Equilateral | PASS |
| 2 | (5, 5, 5) | Equilateral | Equilateral | PASS |
| 3 | (100, 100, 100) | Equilateral | Equilateral | PASS |
| 4 | (5, 5, 3) | Isosceles | Isosceles | PASS |
| 5 | (3, 5, 5) | Isosceles | Isosceles | PASS |
| 6 | (5, 3, 5) | Isosceles | Isosceles | PASS |
| 7 | (10, 10, 15) | Isosceles | Isosceles | PASS |
| 8 | (2, 3, 4) | Scalene | Scalene | PASS |
| 9 | (5, 7, 9) | Scalene | Scalene | PASS |
| 10 | (13, 15, 20) | Scalene | Scalene | PASS |
| 11 | (3, 4, 5) | Scalene Right | Scalene Right | PASS |
| 12 | (5, 4, 3) | Scalene Right | Scalene Right | PASS |
| 13 | (5, 12, 13) | Scalene Right | Scalene Right | PASS |
| 14 | (8, 15, 17) | Scalene Right | Scalene Right | PASS |
| 15 | (1, 1, 1.414...) | Isosceles Right | Isosceles Right | PASS |
| 16 | (5, 5, 7.071...) | Isosceles Right | Isosceles Right | PASS |
| 17 | (1, 2, 3) | Not a triangle | Not a triangle | PASS |
| 18 | (1, 2, 10) | Not a triangle | Not a triangle | PASS |
| 19 | (1, 1, 5) | Not a triangle | Not a triangle | PASS |
| 20 | (10, 1, 1) | Not a triangle | Not a triangle | PASS |
| 21 | (0, 5, 5) | Not a triangle | Not a triangle | PASS |
| 22 | (5, 0, 5) | Not a triangle | Not a triangle | PASS |
| 23 | (5, 5, 0) | Not a triangle | Not a triangle | PASS |
| 24 | (0, 0, 0) | Not a triangle | Not a triangle | PASS |
| 25 | (-1, 5, 5) | Not a triangle | Not a triangle | PASS |
| 26 | (5, -1, 5) | Not a triangle | Not a triangle | PASS |
| 27 | (5, 5, -1) | Not a triangle | Not a triangle | PASS |
| 28 | (-1, -1, -1) | Not a triangle | Not a triangle | PASS |
| 29 | (1, 1, 1) | Equilateral | Equilateral | PASS |
| 30 | (100, 150, 200) | Scalene | Scalene | PASS |
| 31 | (2, 3, 4) | Scalene | Scalene | PASS |
| 32 | (2.5, 3.5, 4.5) | Scalene | Scalene | PASS |
| 33 | (2.5, 2.5, 2.5) | Equilateral | Equilateral | PASS |
| 34 | (5, 5, 5.1) | Isosceles | Isosceles | PASS |
| 35 | (10, 10, 1) | Isosceles | Isosceles | PASS |

**Test Summary:**
- Tests Planned: 35
- Tests Executed: 35
- Tests Passed: 35
- Tests Failed: 0
- Defects Found: 0 (functional)
- Code Quality Issues Fixed: 1
- Pass Rate: 100%

**Analysis:** All tests passed successfully after code quality improvements. No regressions were introduced. The improvement (moving file output to main block) enhances code organization without affecting functionality.

---

### 6. Summary Results Matrix

|  | Test Run 1 | Test Run 2 |
|---|---|---|
| **Tests Planned** | 35 | 35 |
| **Tests Executed** | 35 | 35 |
| **Tests Passed** | 35 | 35 |
| **Defects Found** | 0 | 0 |
| **Defects Fixed** | 0 | 1 (code quality) |

### Testing Strategy - When Did I Have Sufficient Test Cases?

I determined test sufficiency using multiple criteria:

**1. Coverage Criteria Met:**
- All equivalence classes covered (Equilateral, Isosceles, Scalene, Right, Invalid)
- All boundaries tested (minimum, maximum, edge of validity)
- All combinations tested (each pair combination, multiple parameter orders)

**2. Risk-Based Analysis:**
Focused on high-risk areas:
- Right triangle detection (complex logic with floating-point) - 6 tests
- Invalid inputs (critical for robustness) - 12 tests
- Edge cases (boundary conditions) - 5 tests

**3. Confidence Level:**
After 35 tests with 100% pass rate across all categories, achieved high confidence that the function correctly implements triangle classification with proper edge case handling.

**4. Diminishing Returns:**
Additional tests beyond 35 would likely be redundant as all major scenarios, boundaries, and combinations were already tested.

**Strategy Used:**
1. Equivalence partitioning to identify test categories
2. Boundary value analysis to find edge cases
3. Combination testing for thorough coverage
4. Organized tests into logical groups
5. Documented each test's purpose

**Result:** 35 strategically selected tests providing comprehensive coverage with high confidence in the implementation.

---

### Techniques and Assumptions

**Testing Techniques Used:**

1. **Equivalence Partitioning:** Divided input space into valid triangles (Equilateral, Isosceles, Scalene, Right) and invalid triangles (negative/zero values, triangle inequality violations)

2. **Boundary Value Analysis:** Tested minimum values (1,1,1), large values (100,150,200), degenerate cases (1,2,3), and just barely valid triangles

3. **Combination Testing:** Tested all pair combinations for isosceles triangles, different parameter orders for right triangles, and all positions for invalid values

**Assumptions:**
- Function accepts both integer and floating-point values
- Right triangles identified using Pythagorean theorem with tolerance (1e-6)
- Function returns string values for triangle types
- Combined types use format "Type Right" (e.g., "Scalene Right")
- Invalid triangles return "Not a triangle"

**Constraints:**
- All side lengths must be positive (> 0)
- Triangle inequality must hold: a + b > c, a + c > b, b + c > a
- Floating-point comparisons use tolerance of 1e-6
- Function signature: classify_triangle(a, b, c)

**Data Inputs Used:**
Test data was strategically selected from each equivalence class including Pythagorean triples (3-4-5, 5-12-13, 8-15-17), boundary values, floating-point values, and comprehensive invalid input combinations.

---

## 6. Additional Information

### Tools and Environment

- **Language:** Python 3.x
- **Testing Framework:** unittest (Python standard library)
- **Version Control:** Git
- **Repository Hosting:** GitHub
- **Development Environment:** VS Code

### Testing Approach

- Unit testing with unittest framework
- Test-driven validation approach
- Code inspection and manual review
- Regression testing after improvements

---

## 7. Repository Submission

**Repository Name:** hw-06b

**Repository URL:** https://github.com/ssonare/hw-06b

**Files Included:**
- Triangle.py - Improved triangle classification implementation
- TestTriangle.py - Enhanced test suite with 35 test cases
- TestReport1.md - Test results against original implementation
- TestReport2.md - Test results against improved implementation
- test_run1_output.txt - Part 1 test execution output
- test_run2_output.txt - Part 2 test execution output
- CodeInspectionReport.md - Detailed code analysis
- SUBMISSION.md - This comprehensive assignment summary
- README.md - Repository documentation
- output.txt - Example execution output
- .gitignore - Git ignore configuration

**Git Commits:**
- Initial commit: Original Triangle.py and TestTriangle.py files
- Part 1 commit: Enhanced test suite with 35 comprehensive test cases
- Part 2 commit: Code quality improvement and final testing
- Final commit: Documentation and assignment summary

---

## 8. Conclusions

This assignment successfully demonstrated:

1. **Comprehensive Testing:** Developed 35 strategic test cases providing thorough coverage using equivalence partitioning and boundary value analysis

2. **Quality Assessment:** Identified that the original implementation was functionally correct through systematic testing and code inspection

3. **Code Improvement:** Made code quality enhancements while maintaining functional correctness and ensuring no regressions

4. **Professional Process:** Followed industry-standard software testing workflow: test, inspect, fix, retest, document

5. **Documentation:** Created detailed test reports and comprehensive documentation for reproducibility and future reference

**Final Verdict:** The Triangle.py implementation is correct, robust, and production-ready. The enhanced test suite provides ongoing regression testing capability with 100% pass rate confidence.

---

**Assignment Completed:** October 24, 2025
**Total Development Time:** Approximately 3-4 hours
**Status:** ✓ COMPLETE - All parts finished successfully
