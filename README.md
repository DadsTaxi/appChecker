# appChecker

**Warning**
NO WARRANTY. USE AT OWN RISK.

## Functionality
A workflow is defined in this repo that does the following
1. Reads a list of organizations using REST Api (this is currently hard-coded for this demo)
1. Reads secrets ```LISTINSTALLS_APPID``` and ```LISTINSTALLS_SECRET```
1. Gets a JWT token using the App credentials
1. User the JWT token to validate each organization has the app installed
1. If the app is not installed then a GitHub issue is raised

## Setup
1. Create a GitHub App and install in this organization (note the appid)
1. Download the PEM file for the app
1. Set Organization secret ```LISTINSTALLS_APPID``` to the app id of the app you created
1. Set Organization secret ```LISTINSTALLS_SECRET``` to the contents of the PEM file

## Example output
The output below shows 4 organizations being validated.

The first 2 organizations are validated ✅

The next organization do not have the app installed and the last one is where an organization does not exist 

><img width="1162" alt="image" src="https://user-images.githubusercontent.com/107459714/231984971-bc0ceffd-47be-435a-9a4b-836cafb28650.png">

###

### Org does not exist or app not installed
><img width="573" alt="image" src="https://user-images.githubusercontent.com/107459714/231986017-5039c9dc-3b25-41ad-a901-20451ff63de0.png">

### Example issue
><img width="1472" alt="image" src="https://user-images.githubusercontent.com/107459714/231986289-9dfe7153-8fa1-4d08-87f0-565303947259.png">
