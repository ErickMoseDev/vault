# Rails Generators
- rails generate or rails g is used to show you all the generators that come baked-in
- the key generators that we will mostly focus on include:
        --- model
        --- resource
        --- scaffold

### Model
This is the simplest of the generators in that it generates the following files:
--- a model with the name specified
--- a migration for the model

* The command used to run the generator is:

` rails g model ModelName options:type `

* Example to create a note model we write the command as follows:

` rails g model Note title:string body:string --no-test-framework `

The following files were created:
- note.rb
- 20221121163028_create_notes.rb


### Resource
Using the rsource generator gives us more when it comes to generation of files. The following files are generated:
--- a migration
--- model with the name specified
--- a controller in the controller folder
--- opens up all the routes in the config/routes folder


The command to do so is :
` rails g resource User name:string user_name:string email:string `

The following files will be generated :
- db/migrate/20221121164153_create_users.rb
- user.rb
- users_controller.rb
- resources :users

### Scaffold
A Scaffold is a set of automatically generated files which forms the basic structure of a rails project. These files include:
- A controller -> contains the basic methods for a crud operation
- A model
- migrations
- opens up all the routes in config/routes

The command to do so is :
` rails g scaffold Project name:string desc:string `

The following files were generated:
- db/migrate/20221121170226_create_projects.rb
- project.rb
- projects_controller.rb (a scaffold_controller - comes with more methods generated inside the controller file)
- resources :projects