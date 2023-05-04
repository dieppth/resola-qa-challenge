# How to run the test
## Testing tools:
- Postman
- Or Newman
## Precondition:
- Have Postman install/login in the computer
- Or have Newman install in the computer
- Install html report for newman in the same folder of API Collection folder.
    - Guide: https://learning.postman.com/docs/collections/using-newman-cli/installing-running-newman/
- Download and extract file Diep_Assignment.zip
##Introduction:
- Diep_Assignment.zip contains:
    - 1 postman collection json file
    - 2 set of data test json file
    - 1 folder “newman” to contain html report if running the test by newman
- There are 2 folders in the API collection, they have different test objectives and use different test data sets.
   - The API “Track API - Test” objectives:
      - Verify the API response body with status code 200
      - Verify the API response body with status code 400
      - Verify the validation of mandatory and non-mandatory request params
   - The API “Track API - Test Data Type objectives:
      - Verify the validation of data type for each param in the request body.

# Steps to run the test:
### Using Postman tool
1. Open Postman
2. Import “Diep Assignment - Track.postman_collection.json”, if successfully you will see the collection like this:
3. Hover “Track API - Test” folder and click Run folder
4. Select the iteration data file “test-data-Track API - Test.json, you will see:
5. Click button Run => finish the test objective of  “Track API - Test”
6. Hover “Track API - Test Data Type” folder and click Run folder
7. Select the iteration data file “test-data-Track API - Test Data Type.json, you will see:
8. Click button Run => finish the test objective of  “Track API - Test Data Type”
### Using Newman tool
1. Open command line
2. Locate to the folder “Diep_Assignment” that you have extracted
3. Use command: `newman run "Diep Assignment - Track.postman_collection.json" --folder "Track API - Test" -d "test-data-Track API - Test.json" -r html`
4. Hit Enter => finish the test objective of  “Track API - Test”. Then you can see the report in the folder “newman”
5. Use command: `newman run "Diep Assignment - Track.postman_collection.json" --folder "Track API - Test Data Type" -d "test-data-Track API - Test Data Type.json" -r html` 
6. Hit Enter => finish the test objective of  “Track API - Test Data Type”. Then you can see the report in the folder “newman”







