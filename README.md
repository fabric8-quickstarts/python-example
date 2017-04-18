# python-example
Example python application running on fabric8.A simple blog application using python's web.py framework.

The blog is stored in MySQL database.

### Running the app locally
- Instal MySQL database server on your machine and create database blog
- Clone the repository
- Install all the requirements by `pip install -r requirements.txt`
- Start the application with the following command `python blog.py`
- Open your brower and you will see your blog application running on http://localhost:8080

### Running the app on Openshift
- Clone the repository
- Login to Openshift using `oc login` on your terminal
- Create a new project, for eg : foo using `oc new-project foo`
- Create the application on Openshift using `oc new-app -f ~/python-blog/openshift/python-mysql-template.yaml -p NAMESPACE=foo`
- Check the status of the app using `oc status`
- Open the Openshift console you will see two services comming up one for the database and other for the python blog app. Click on
  the route to check if the application is deployed.
