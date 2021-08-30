# Introduction
* A **Test Management Solution** using Markdown files and GitHub.
* You could change test specifications or upload test results anywhere with a browser. Then reports will be generated automatically in `Reports` folder using GitHub Actions.
* Step-by-step instructions can be found in the below video


  https://user-images.githubusercontent.com/25169430/131285088-3412bc3c-2afb-4668-86a2-09d2693a1a1a.mp4


# Step by step
## 1. Clone template repository and enable GitHub Action
* Using this template (including pre-configured GitHub Actions, report library and Test Specification template), it is easy to create a minimal Test Management solution
* User must have a GitHub account  
  
1.1. Login your [GitHub](https://github.com/login) account  
1.2. Open https://github.com/lgjp-open-source/TestManagementSolution in a new tab and click `Fork` button on the top right of opened tab  
1.3. Click `Actions` tab, then click `I understand my workflows, go ahead and enable them` button

## 2. Create and update Test Specification Markdown files (customize a Markdown file)
2.1. Create a new Test Specification Markdown file  
 * Click `TestManagementSolution/Tests/` folder
 * Click `Template.MD` file, then open edit mode by click Pen symbol on the right. Select all file content and copy it  
 * Go back to `TestManagementSolution/Tests/` folder
 * Click button `Add file`, then click `Create new file`
 * Enter your Markdown file name and location (for example: `./Tests/GeneralTest.MD` or `./Tests/basic/ChromeTest.MD`)
 * Paste the content copied in the above step to this new file
 * Click `Commit new file` button to save this file
 * Your Markdown file look like
 ![Markdown](https://user-images.githubusercontent.com/25169430/131081891-4563eb4f-fc63-4819-a3a7-063db19fb6c6.png)  

2.2. Fill test case design
* Open your Markdown file (create in step 2.1 above) in edit mode by click Pen symbol on the right
* Enter test design information (Blue fields in the above picture)
  * Test Case information:
    * Enter your test case id to the unordered list below "## Test Case ID" header - replace "N/A" value
    * Enter your test case script location to the unordered list below "## Test Script Location" header - enter the meaningful informative, otherwise leave it as N/A
    * Enter your test case name to the unordered list below "## Test Case name" header - replace "N/A" value
    * Enter your test case description to the unordered list below "## Test Case Description" header - enter the meaningful informative, otherwise leave it as N/A
  * Test Criteria:
    * Enter your test case pre-conditions to the unordered list below "## Pre-conditions" header - enter the meaningful informative, otherwise leave it as N/A
    * Enter your test case post-conditions to the unordered list below "## Pre-conditions" header - enter the meaningful informative, otherwise leave it as N/A
  * Test Steps: 
    * Enter your test step details to the unordered list below "* Step Details" unordered list - enter the meaningful informative(for example: login with valid credential), otherwise leave it as N/A
    * Enter your test step data to the unordered list below "* Test Data" unordered list - enter the meaningful informative(for example: username=test, password=123456), otherwise leave it as N/A
    * Enter your test step expected results to the unordered list below "* Expected Results" unordered list - enter the meaningful informative(for example: login successful), otherwise leave it as N/A
  * If you have more than one step, copy "Step 1" ordered list and enter test step details, test step data and test step expected results again
* Click `Commit changes` button to save your test design  

2.3. Fill test results
* Assume that you already run your test and have result
* Click your Markdown file in step 2.2 above and open it in edit mode
* Enter test results information (Yellow fields in the above picture)
  * Enter your test date to the unordered list below "## Date Tested (mm/dd/yy hh:mm:ss)" header - replace "N/A" value, for example: 8/18/21 18:20:59
  * Enter your test results to the unordered list below "## Test Case Results (Pass / Fail / Not executed / Suspended))" header - replace "N/A" value with Pass, Fail, Not executed, or Suspended
  * Enter your test step actual result to the unordered list below "* Actual Results" unordered list - enter the meaningful informative (for example:login successful), otherwise leave it as N/A
  * Enter your test step result to the unordered list below "* Pass / Fail / Not executed / Suspended" unordered list - replace "N/A" value with Pass, Fail, Not executed, or Suspended

* Click `Commit changes` button to save your test design

## 3. View Test Reports
Reports are generated automatically in `./Reports` folder (by GitHub Actions) when repository changes
* Once you have updated & committed your test results per describe in Fill test results,  on your Github repo, select 'Action' Tab
* Wait for the analysic process finished (the lastest workflow runs in the table change from yellow to green)
* Click `./Reports/TotalAnalysis.MD` to view test reports
* There are more reports that you could explore in [Advance](./advance.md) topic
