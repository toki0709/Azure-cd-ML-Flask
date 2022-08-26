# Overview

<TODO: complete this with an overview of your project>

## Project Plan
<TODO: Project Plan

* A link to a Trello board for the project
* A link to a spreadsheet that includes the original and final project plan>
	
## Instructions

* Architectural Diagram of workflow
  - CI workflow
 
     ![CI part](https://user-images.githubusercontent.com/61994831/186890022-95444de6-ffdd-47ef-a742-c1af6089052c.jpg)

  - CD workflow

	![arc app](https://user-images.githubusercontent.com/61994831/186885789-bdc498dc-b1f3-4f18-b6f5-ed57016c5017.jpg)


<TODO:  Instructions for running the Python project.  How could a user with no context run this project without asking you for any help.  Include screenshots with explicit steps to create that work. Be sure to at least include the following screenshots:
* Log into azure and click on cloud shell and select bash.
* generate SSH key and add it to github account.
* Clone Git repository 

	![azure cloud shell](https://user-images.githubusercontent.com/61994831/186887833-a43d65e6-f94c-44bc-84c5-649837e65f54.jpg)

* Create and activate virtual environment for the project to install all the required libraries and packages from requirements.txt file.
  - python3 -m venv ~/.venv-name
  - source ~/.venv-name/bin/activate
* Go to the project directory and run 'make all'. This will install and run python test for the project.
  - Installing packages
 ![Inkedmakeall_1](https://user-images.githubusercontent.com/61994831/186888675-a39576bd-e4fe-46ec-8d1d-b0a47e2b1db5.jpg)
 
  - Running tests
 ![makeall_2](https://user-images.githubusercontent.com/61994831/186888771-73f673b1-49ea-44aa-b592-742140ad264f.jpg)

* Enable GitHub Action to test the project every time there are any chages in code.


	- ![remote_test_pass](https://user-images.githubusercontent.com/61994831/186892663-af7f7449-2b3c-40ff-a463-85061326b3c8.jpg)


* Project running on Azure App Service
* Create the webapp with the command az webapp up --name [webapp name] --resource-group [RG name] --sku [F1]. This will create our webapp.
* After successful creation we can add the name of our webapp in ./make_predict_azure_app.sh file.
* After all the dependencies are installed in the environments, now run python app.py. This will trigger the flask ml app.

* Running Azure App Service from Azure Pipelines automatic deployment
	- On Azure DevOps create new project and select Git based version control
	- Create a new pipeline and select the github repo with the flask ml app.
	- Configure the pipeline. For this project .yml file is already provided.
	- Check if the newly configured .yml file is in the github project repo.
	- run the pipeline. Successful deployment will be as follow:
		- Successful deploy of the project in Azure Pipelines.
	
		![deployment](https://user-images.githubusercontent.com/61994831/186898613-a949c651-833c-4b79-8ad2-df5ad184d821.jpg)


* Successful prediction from deployed flask app in Azure Cloud Shell
	- Create two separate bash window and in one run python app.py and on another window run ./make_predict_azure_app.sh file.
The output should look similar to this:

![prediction](https://user-images.githubusercontent.com/61994831/186895517-1bfebe79-a88a-4dcd-b383-d4e4c65697a9.jpg)

* Output of streamed log files from deployed application

> ![logtail](https://user-images.githubusercontent.com/61994831/186896826-7cf7cd22-ac06-485f-811b-7dd09361dc8a.jpg)

## Enhancements
	- Look into python library version. Some libraries might be deprecated.
	
## Demo 

<TODO: Add link Screencast on YouTube>


