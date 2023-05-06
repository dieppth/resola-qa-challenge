# How to run the test
## Testing tools:
- Postman
- Or Newman
## Precondition:
- Have Postman install/login in the computer
- Or have Newman install in the computer
    - Install html report for newman in the same folder of API Collection folder.
    - Guide: https://learning.postman.com/docs/collections/using-newman-cli/installing-running-newman/
- Download the collection file `Diep Assignment - Track.postman_collection.json`
- Download 2 iteration files: `test-data-Track API - Test Data Type.json`, `test-data-Track API - Test.json`

## Introduction:
When importing successfully the Diep Assignment - Track" collection in Postman, you will see 2 folders, they have different test objectives and use different test data sets.
- The API “Track API - Test” objectives:
   - Verify the API response body with status code 200
   - Verify the API response body with status code 400
   - Verify the validation of mandatory and non-mandatory request params
- The API “Track API - Test Data Type objectives:
   - Verify the validation of data type for each param in the request body.

# Steps to run the test:
### Using Postman tool
1. Open Postman
2. Import “Diep Assignment - Track.postman_collection.json”, if successfully you will see the collection like this: ![Import Collection](/images/collection.png)
3. Click Run folder “Track API - Test” folder
4. Select the iteration data file `test-data-Track API - Test.json`, you will see: ![Run Test Objective 1](/images/trackapi.png)
5. Click button Run => finish the test objective of  “Track API - Test”
6. Click Run folder “Track API - Test Data Type” folder
7. Select the iteration data file `test-data-Track API - Test Data Type.json`, you will see: ![Run Test Objective 2](/images/trackapi-datatype.png)
8. Click button Run => finish the test objective of  “Track API - Test Data Type”
### Using Newman tool
1. Download file Diep_Assignment.zip and extract it.
2. Open command line
3. Locate to the directory “Diep_Assignment” that you have extracted
4. Use command: `newman run "Diep Assignment - Track.postman_collection.json" --folder "Track API - Test" -d "test-data-Track API - Test.json" -r html`
5. Press Enter => finish the test objective of  “Track API - Test”. Then you can see the report in the folder “newman”
6. Use command: `newman run "Diep Assignment - Track.postman_collection.json" --folder "Track API - Test Data Type" -d "test-data-Track API - Test Data Type.json" -r html` 
7. Press Enter => finish the test objective of  “Track API - Test Data Type”. Then you can see the report in the folder “newman”







