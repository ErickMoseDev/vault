# Routing

Routing is a technique by which applications redirect traffic to the correct controllers and handlers
Used widely by apps to organize how data is queried and navigated inside the app.

#### What are Resources?

A resource is any object that can be accessed via a Uniform Resource Index (URI) and is expected to take in
crud operations via user is known as a resource.
In the case of ruby, it is generally a database table, which can be represented by a model and accessed by a controller

#### The Routing File

routes.rb is a file that takes care of all the routing inside our application. Thos is done by charting out how resources are
mapped to the available routes.

if we were to route a Post resource, the routes would look like this:

```
Rails.application.routes.draw do
  resources: posts
end

```
VERB        PATH            Controller#Action           Used for
GET         /posts          posts#index                 display a list of all posts
POST        /posts          posts#create                create a new post
GET         /posts/:id      posts#show                  display a specific post
PATCH/PUT   /posts/:id      posts#update                update a specific post
DELETE      /posts/:id      posts#destroy               delete a specific post