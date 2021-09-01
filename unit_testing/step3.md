## Output Format

1. Excel Output

To allow the test results to be exported to excel format, install `pytest-excel` using `pip install`:
> `pip install pytest-excel`{{execute}}

Run tests and report the result in excel format:
> `pytest -v --excelreport=report.xlsx`{{execute}}

![Picture 5](./assets/pic5.png)

Open the generated excel document:

![Picture 6](./assets/pic6.png)

2. XML Output

To output the test results in XML format:
> `pytest  --junit-xml test-reports/results.xml`{{execute}}

In this example, **pytest** is running without specifying the test script. It will scan all the test scripts (e.g. python scripts with the name ending with \_test)  in the folder and execute all the test methods.

<br/>
