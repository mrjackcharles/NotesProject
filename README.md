# Jack's NotesApp


This application is a basic notes app with several features:

- Ability to sign up and create your own account so that your notes are personal and cnba only be accessed withan email and passowrd

- Sign in functionailty to view your notes

- Ability to create new notes and save them to your account

- Delete any notes that you do not want anymore

- Logout of your account when finishe creating your notes


Description of how the app works:
- This is a flask application build using primarily python code. This app also includes html for the webpage formatting. It also has one javascript file for the deletion of notes. A dockerfile is used within the application to build it as well as a docker-compose file to deploy the app. 
- The formatting of the webiste uses several bootstap links in base.html in order to create a satisfiying UI.

- The database is stored on the same vm as the application


Overall Environment diagram:
![NoteAppEnv](https://user-images.githubusercontent.com/92857396/146536408-cb2ecb61-e11d-4d2d-9ba3-18e06e926245.png)

- This application is hosted on an azure vm

For Future:

- For Jenkins to deploy the updates app automatically (current only gives vm new dockerhub image)
- Create a Swarm for app on cloud
- Create database in cloud on seperate vm

------
