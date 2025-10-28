# 🧪 Final Group Test Report Template — Word Puzzle Game Plus

**Level:** Intermediate QA | **Week 5:** Test Management

**Course:** Software Testing & Quality Assurance  
**Module:** Test Management (Week 5)  
**Project Type:** Group Assessment  
**Submission Date:** 2025-10-28

## Team Information

| Role | Name | Responsibilities |
|------|------|------------------|
| Test Manager | Eunice| Planning, scheduling, coordination, metric tracking |
| Risk Analyst |Nadwa | Risk identification, prioritization, test design linkage |
| Test Executor | Kevin| Execution, evidence capture, defect logging |

## Project Overview

**System Under Test:** Word Puzzle Game Plus  
**Technology Stack:** HTML, CSS, JavaScript  
**Environment:** Chrome Browser (Desktop)

### Features Under Test

| Feature | Description | Risk Category |
|---------|-------------|---------------|
| Reset Game | Clears score and progress instantly | low|
| Leaderboard | Stores top 3 scores in localStorage | low|
| Bonus Round | Every 3 puzzles → doubles score | low|

## Test Plan
- Application: Word Puzzle Game Plus
T- est Approach: Risk-based testing with prioritization

### Scope

**In Scope:**
- Testing Scope: Functional, UI/UX, Compatibility, Performance, Security

### Tools & Resources

- Manual testing, Browser DevTools, GitHub Issues for tracking

### Schedule

| Phase | Planned Duration | Actual Duration | Status |
|-------|------------------|-----------------|--------|
|Test Planning & Preparation|	3 days|2days|	completed|
|High Priority Testing|	5 days|	2days|inprogress|
|Medium Priority Testing|	3 days|	2days|inprogress|
|Low Priority Testing|	2 days|	1day|completed|
|Defect Retesting & Regression|	3 days|3days|	completed|
|Test Summary & Reporting|	1 day|	inprogress|inprogress|


## Risk Analysis

### Risks

| ID | Feature | Risk Description | Likelihood | Impact | Priority | Mitigation Strategy |
|----|---------|------------------|------------|--------|----------|---------------------|
|R-001	|Scoring System|	Incorrect point calculation for hint usage and bonus rounds|	High	|High|	P1	|Implement unit tests for scoring logic; manual validation of all scoring scenarios|
|R-002|	Word Scrambling|	Algorithm may not properly scramble words or create unsolvable puzzles	|Medium|	High|	P1	|Test scrambling with various word lengths; validate all words remain solvable
|R-003	|Local Storage|	Leaderboard data corruption or loss on browser refresh	|Medium|	High|	P1	|Implement data validation; test storage limits; add error handling for parse failures
|R-004|	Browser Compatibility|	Inconsistent behavior across different browsers	|High	|Medium|	P2	|Early cross-browser testing; use feature detection; progressive enhancement
|R-005	|Responsive Design|	UI breaks on mobile devices or unusual screen sizes	|Medium|	Medium|	P2|	Test on multiple devices; use responsive design testing tools
|R-006	|Accessibility	|Game not usable for users with disabilities	|Medium	|Medium	|P2	|Conduct accessibility audit; test with screen readers; keyboard navigation testing
|R-007	|Input Validation	|Malicious input could break game functionality|	Low|	High	|P2|	Implement input sanitization; test with special characters and long inputs
|R-008	|Performance|	Game becomes slow with extended play or large word banks	|Low	|Medium	|P3|	Monitor memory usage; test with extended gameplay sessions
|R-009	|Visual Consistency	|Styling inconsistencies across different states|	Low	|Low|	P3|	Create visual regression tests; consistent design review


### Risk Coverage

- Tested Risks Percent: 
- Untested Risks Percent: 

## Test Cases

| ID | Feature | Objective | Expected Result | Actual Result | Status | Risk Link |
|----|---------|-----------|----------------|---------------|--------|-----------|
|-001	|Game Initialization	|Verify game starts correctly|Word displayed scrambled, score 0, solved 0|	As expected|	✅ Passed	|R-001,R-002
TC-002|	Correct Guess (No Hint)|	Validate scoring for direct solve	Score +10, solved count +1	|Score +10, solved +1	✅ Passed	R-001
TC-003|	Correct Guess (With Hint)|	Validate scoring with hint usage	Score +3 net (5-2), solved +1|	Score +3, solved +1	✅ Passed	R-001
TC-004|	Bonus Round\	Verify bonus round triggering	|Score doubles every 3 solves|	Score doubled correctly	|✅ Passed|	R-001
TC-005	|Leaderboard|	Test data persistence	|Scores maintained after refresh	|Scores persisted correctly|	✅ Passed	|R-003
TC-101|	|Responsive Design|	Verify layout adaptation|	UI adapts to screen sizes|	Layout responsive at breakpoints	|✅ Passed|	R-005
TC-102	|Keyboard Navigation	|Test accessibility	|All elements keyboard accessible	|Tab navigation works|	✅ Passed	|R-006
TC-103|	Input Validation	Test empty input handling	Error message displayed	|"Please enter a guess!" shown|	✅ Passed|	R-007
TC-SCRAM-001|	Word Scrambling	Verify scramble ≠ original	Scrambled word different	|Words properly scrambled	|✅ Passed|	R-002
TC-SCRAM-002|	Scramble Solvability	Ensure all words remain solvable	All scrambled words solvable	|8/10 words verified solvable|	🔄 In Progress|	R-002
TC-BROW-001	|Chrome Compatibility	Test Chrome functionality	All features work in Chrome	All features functional	✅ Passed	R-004
TC-BROW-002	|Firefox Compatibility	|Test Firefox functionality	|All features work in Firefox	|Minor CSS alignment issues	⚠️ Failed	R-004
TC-ACC-001	|Screen Reader	|Test with screen reader|	ARIA labels read correctly	|Basic labels working|	🔄 In Progress|	R-006
TC-SEC-001|	XSS Prevention	|Test script injection	|Input sanitized, no execution|	Basic sanitization working|	🔄 In Progress|	R-007
 | | | | | | |

## Defects

| ID | Issue Title | Severity | Risk ID | Status | GitHub Link |
|----|-------------|----------|---------|--------|-------------|
| DEF-001	|Firefox CSS Alignment Issue|	Medium	|R-004	|🔄 In Progress	|GitHub #001
|DEF-002	|"javascript" Word Unsolvable When Scrambled|	High	|R-002	|✅ Fixed	|GitHub #002
|DEF-003	|Hint Button Active After Use	|Low	|R-001|	✅ Fixed	|GitHub #003
|DEF-004	|Mobile Touch Target Too Small|	Medium	|R-005	|📋 Backlog	|GitHub #004

## Metrics
- Test Case Pass Percent: 78.6% (11/14 executed test cases passed)

- Defect Density: 0.36 defects/test case (5 defects / 14 test cases)

- Risk Coverage Percent: 72.2% (as previously calculated)

- Regression Success Rate: 100% (2/2 fixed defects passed retest)


### Defect Summary
- Total Defects Logged: 5

- Critical/High: 2 (40%)

- Medium: 2 (40%)

- Low: 1 (20%)

- Fix Rate: 40% (2/5 defects fixed)



## Test Control & Project Management

### Phases

| Phase | Deliverable | Actual Output | Variance | Owner |
|-------|-------------|---------------|----------|-------|
|Test Planning|	Signed Test Plan|	Test Plan v1.2 approved|	+0.5 days|	TM Lead Eunice
|High Priority Testing|	|P1 Test Report|	90% P1 coverage achieved|	On schedule|TM Lead Eunice
|Medium Priority Testing	|P2 Test Report	|75% P2 coverage in progress|	-1 day delay	|RA Lead Kevin
|Defect Resolution|	Critical fixes|	2/2 high severity fixed|	On schedule	|Dev Team
|Regression Testing|	Regression report	|100% pass rate|	On schedule	|TE Lead Nadwa 
 

**Progress Tracking Method:**
- Daily standups with defect review

- GitHub Issues with automated status updates

- Test case execution dashboard in Google Sheets

- Weekly metrics reporting to stakeholders
  
**Change Control Notes:**
- Added 2 additional test cases for scramble validation (approved by PM)

- Extended browser compatibility scope to include mobile Safari (change request #CR-003)

- Postponed performance testing to Phase 2 due to critical defect findings



## Lessons Learned

- Most Defect Prone Feature: 
- Risk Analysis Impact:
a 1-day delay in medium priority testing due to browser compatibility issues

b Two defects requiring immediate attention (DEF-001, DEF-005)

c Accessibility testing taking longer than anticipated
- Team Communication Effectiveness: need to be worked on 
- Improvements for Next Cycle:
 i Complete Firefox compatibility fix (DEF-001)
ii Resolve leaderboard duplicate entries (DEF-005)

iii Finalize scramble solvability testing (TC-SCRAM-002)

iv Complete accessibility audit
  

## Sign Off

| Name | Role | Initials | Date |
|------|------|-----------|------|
|Eunice | Test Manager | TM| 28/10/2025|
|Kevin | Risk Analyst | RA| 28/10/1025|
|Nadwa | Test Executor |TE |26/10/2025 |

## ✅ Achievements
All high-risk functional areas (scoring, basic gameplay) validated

Critical defect DEF-002 (unscrambleable word) resolved

78.6% test pass rate meeting quality gates

Effective defect tracking through GitHub Issues

**Statement:** 
## 📊 Quality Gates Status
text
Test Coverage:    ████████░░ 72.2%  (Meeting Week 1 target)
Defect Resolution: █████░░░░░ 40%   (Below target - needs focus)
Test Pass Rate:   ████████░░ 78.6%  (Meeting minimum 75% requirement)

**Test Status:** ☐ Completed / ✅In Progress / ☐ Deferred
