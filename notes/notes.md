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

  4. Heroku setup

      ensure version of Ruby is known

          amend gemfile and add gem for postgres
          plus production

          amend sqlite3

          add gem 'rails_12factor'

      open config/database.yml
          delete production

      run _bundle install --without production_

  5. Heroku
        login to Heroku in the terminal

            run heroku apps:create _unique name_ (first-payment-rails-app)

            run git push heroku master

            (https://first-payment-rails-app.herokuapp.com)

  6. Add Twitter Bootstrap

        add gem 'bootstrap-sass'

        run bundle install

        add app/assets/stylesheets/bootstrap_custom.css.scss

  7. Improve look of homepage

        open

        app/views/layouts/application.html.erb

        app/views/pages/home.html.erb
          add div code

  8. homepage part 2

        open

        app/views/layouts/application.htlm.erb - amend

        add app/assets/stylesheets/main.css

  9. homepage part 3

        add image to app/assets/images

        set the path in the home.html.erb

        amend image details

        import Bootstrap javascript
        app/javascripts/application.js
        
