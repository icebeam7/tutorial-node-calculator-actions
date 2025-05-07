name: Run Tests and Upload Artifact

on: [push, pull_request]

jobs:
  test:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout code
        uses: actions/checkout@v4

      - name: Setup Node.js
        uses: actions/setup-node@v4
        with:
          node-version: 22

      - name: Install dependencies
        run: npm install

      - name: Run tests and generate report
        run: node test/calculator.test.js

      - name: Upload artifact
        uses: actions/upload-artifact@v4
        with:
          name: test-results
          path: results/test-results.txt
