## Steps:

1. Export the postman test scripts
2. create a package file : npm init
3. download newman package: npm install newman --save

https://learning.postman.com/docs/running-collections/using-newman-cli/command-line-integration-with-newman/

## Jenkin script node stage 
1. git https://github.com/loyolastalin/postman-test-cases.git
2. sh 'npm install'
2. sh 'npm run execute-postman-test-prod'

## Generate Reports normall

1. npm install -g newman-reporter-html
2. newman run apigee-test-cases.postman_collection.json -r html
3. Navigate to the folder and see the generated HTML file

## Generate Reports Advance

1. npm install -g newman-reporter-htmlextra
2. newman run apigee-test-cases.postman_collection.json -r htmlextra
3. Navigate to the folder and see the generated HTML file
