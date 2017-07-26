# A rails application

### Instructions

  1. Ensure that Ruby and Rails are installed on the system.

  2. Generate new Rails application

      rails new _app name_

      check run _rails server_

      navigate to  "http://localhost:3000/"

  3. Create a home page

      a. create a route
        config/routes.rb
          root 'pages#home'
      b. create pages_controller.rb
          app/controllers/pages_controller.rb
            This inherits from the application controller
      c. create new view
          app/views/pages/home.html.erb

  4.
