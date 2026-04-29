# WalletHub - QA Test Summary (Test 1 & Test 2)

## Overview
This project includes two QA test tasks covering functionality and logic validation.

---

## Test 1: Profile Photo Upload
Tested the profile photo upload feature on the WalletHub settings page.

### Coverage:
- File types: JPG, PNG, GIF, invalid (PDF, EXE)
- File size and image resolution
- Multiple uploads and replacement behavior
- Invalid and edge cases

### Validation:
Each upload was verified by checking if the image appears correctly on the profile page.

---

## Test 2: Account Diversity Grade
Validated grading logic based on:
- `loanTypeCount` (distinct valid loan types)
- `totalAccounts` (excluding Collections & Unknown)

### Grading Rules:
- A → totalAccounts > 20 OR loanTypeCount ≥ 4  
- B → totalAccounts > 10 OR loanTypeCount = 3  
- C → totalAccounts ≥ 5 OR loanTypeCount = 2  
- D → totalAccounts > 0 OR loanTypeCount = 1  
- null → no valid accounts  

### Coverage:
- Users U1–U9 cover all grades (A, B, C, D, null)
- Includes boundary cases (10, 20, >20)
- Validates exclusion rules

---

## Result
- Test 1: Upload feature validated across multiple scenarios  
- Test 2: All grading conditions and edge cases verified  

Both tests confirm correct functionality and robustness.
