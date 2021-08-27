# 1. Create Test Specification Markdown files

### 1. Rules
* All Test Specification Markdown file must place in `./Tests` folder or sub-folder
* `Test Case ID`, `Test Case Script's location`, `Test Case Name`, `Test Case Description`, `Pre-condition`, `Post-Condition`, `Step Details`, `Test Step's Data`, or `Test Step Expected Results` fields in Markdown file use for test design (blue rectangle in the following picture)
* `Date Tested (mm/dd/yy hh:mm:ss)`, `Test Case Results`, `Actual Results` or `Pass / Fail / Not executed / Suspended` fields in Markdown file use for upload results (yellow rectangle in the following picture)
* `Date Tested (mm/dd/yy hh:mm:ss)` field is mandatory and unique
 ![Markdown](https://user-images.githubusercontent.com/25169430/131081891-4563eb4f-fc63-4819-a3a7-063db19fb6c6.png)
### 2. Create Test Design
* Test Design must follow the template

### 3. Upload Test Results
* The person upload results (commit results) is the "Tester's Name" when convert to Excel
* Remember that `Date Tested (mm/dd/yy hh:mm:ss)` field is mandatory and unique

### 4. Pull Request
* If your Test Design needs approvement from other Designer, create a Pull Request instead of commit directly to the repository
* The person that complete the merge is the "Reviewed By" person when convert to Excel

### Demo Video


https://user-images.githubusercontent.com/25169430/130926281-f057e44b-a519-4986-a2b3-b4fbeb7bd0c6.mp4


# 2. Test Reports
Reports are generated automatically in ./Reports folder (by GitHub Actions) when repository changes. There are 3 type of reports:
### 1. Test Case Specification in Excel format
* Each Test Case Specification Markdown file has a corresponding Excel file
* It is converted from Markdown file (automatically when Markdown file changes) for friendly view and report
* For example: `./Tests/basic/ChromeTest.MD` has a corresponding Excel file `./Reports/basic/ChromeTest.xlsx`
![TestCaseExcell](https://user-images.githubusercontent.com/25169430/130310307-6a985458-52d5-4320-bf50-8223574f3519.png)

### 2. Test Summary Report
* Generated automatically in ./Reports/TotalAnalysis.xlsx file or ./Reports/TotalAnalysis.MD file (same information but in different format)
* Contains a summary of all test cases and final test results of a testing project, including:
  * Total number of test cases, number of failed tests, number of passed tests ...
  * List of test cases(Test ID, Test Name, Date Tested, Test Results)
* A Markdown sample file
![MarkdownTotalAnalysis](https://user-images.githubusercontent.com/25169430/130310156-10e1c847-cd5e-4f4e-820e-09fb5b67168b.png)
* An Excel sample file
![ExcelTotalAnalysis](https://user-images.githubusercontent.com/25169430/130310133-c0a52e45-1d55-4ed3-bfd0-180e0187f613.png)

### 3. Test Run History Report of a Test Case
* Each Test Case has a corresponding Run History Report in Excel file and Markdown file (same information but in different format)
* Generated automatically in {TestCaseName}Analysic.xlsx file or {TestCaseName}TotalAnalysis.MD file
* For example: `./Tests/basic/ChromeTest.MD` has a corresponding Markdown file `./Reports/basic/ChromeTestAnalysic.MD` and Excel file `./Reports/basic/ChromeTestAnalysic.xlsx`
* Contains a summary of all test run history of a test case, including:
  * Total number of test run history results: Test ID, Test Name, number of failed tests, number of passed tests ...
  * List of test history runs(Date Tested, Test Results)
* A Markdown sample file
![AnAnalysisMD](https://user-images.githubusercontent.com/25169430/130310238-f7000ee0-caa2-4f3b-9a18-324b19343f9c.png)
* An Excel sample file
![AnAnalysisExcel](https://user-images.githubusercontent.com/25169430/130310233-d2e3ffe1-aac7-4bf8-a83f-4d563467c7e1.png)

### Demo Video

https://user-images.githubusercontent.com/25169430/130919925-c388018c-80cd-4835-b2ca-1a8bd785dffc.mp4

