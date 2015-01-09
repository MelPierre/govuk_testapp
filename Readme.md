# test ruby application using the following gems

* gem 'govuk_template'
* gem 'govuk_frontend_toolkit'


# To see a working page complete the following:

In layout/ application.html.erb   replace everything with:

<% content_for :stylesheets do %>

  <%= stylesheet_link_tag "application", media: "all" %>

<% end %>

<% content_for :javascripts do %>

  <%= javascript_include_tag "application" %>

<% end %>

<%= render template: "layouts/moj_template" %>

Add a controller to test (static_controller.rb)

class StaticController < ApplicationController
end

Add new folder and view to test (static / home.html.erb)

* App Name
* First name: input box
* Last name:input box
* Submit button using value="Submit" class='button'

Add a route in routes.rb to point to page

root to: 'static#home'

Save the project, start server and check project is working, with the start page at on  (http://0.0.0.0:3000).


In the asset pipeline add reference to the toolkit

* //=require govuk_toolkit
* *= require design-patterns/_buttons
* *= require _colours

