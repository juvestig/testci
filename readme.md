# Test app for CI/CD with verbose cURL for docker hub trigger

This is a test replica of quick and dirty test node.js app cobbled together for the purposes of demonstrating a basic CI/CD workflow with Docker Hub for a Pluralsight test course.

## Here's the corrected syntax for Docker hub trigger from Circle CI cURL

#### Original from test tutorial-
curl -H "Content-Type:application/json" --data '{"build":true}' -X POST https://registry.hub.docker.com/u/juvesaurabh/testci/trigger/8f33c63c-15ad-4e4c-b1fa-8c4808557cc6/


#### FROM FORUM--
curl --request POST --header Content-Type:application/json --data {"build":true} --url https://registry.hub.docker.com/u/juvesaurabh/testci/trigger/8f33c63c-15ad-4e4c-b1fa-8c4808557cc6/

#### THIS WORKS (no single quotes and syntax update)-
curl --verbose --trace-time --header Content-Type:application/json --data {"build":true} -X POST https://registry.hub.docker.com/u/juvesaurabh/testci/trigger/8f33c63c-15ad-4e4c-b1fa-8c4808557cc6/

