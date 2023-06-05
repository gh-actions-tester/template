# Automated Testing Template Repository

This template repository is equipped with a workflow and utilities intended to streamline the testing process for each assignment and update the Firestore database with the results automatically.

## How to Use

1. **Fork or Download this template repository.**

2. **Upload your test files.**
   - The tests should generate a `test-output.xml` file using **JUnit XML** in the root directory (or you can adjust the path as needed).

3. **Activate Github Actions within the repository.**

4. **Customize the workflow to match your testing requirements.**
   - Open the GitHub workflow configuration file located at `.github/workflows/main.yml`.
   - Adjust the file to match your project's specific needs:
     - Modify the command to install dependencies,
     - Adjust the command to run your tests,
     - Amend the path to your JUnit XML output file.
   - Commit and push these changes to your main branch.

5. **Test the pipeline.**
   - Upload your solution file to a new branch.
   - Upload your solution files on the assignment page.
   - Check Github Actions to ensure that the results are being accurately uploaded to the database. 

## Example Use Case - JavaScript

Assuming `index.js` is the solution file to be uploaded. It should be placed in the root directory.

1. Fork the template repository, ensuring the organization remains as the owner.

2. Establish a testing environment within the `/tests` folder. For example, `sum.test.js`.

3. Enable Github Actions within this repository.

4. Create a new script inside the test to generate a JUnit XML file.
```
"scripts": {
"test": "jest --reporters=default --reporters=jest-junit"
}
```

5. Modify the Github workflow to:
   - Install the necessary testing dependencies,
   - Execute the tests.
   
6. Verify the pipeline by uploading the solution file on the assignment page and inspecting the workflow results within Github Actions.
