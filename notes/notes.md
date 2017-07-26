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

  10. Update layout

        open home.html.erb

        take div code and transfer to application

        push changes to heroku

  11. Credit Card Form

        Using Stripe

        Add gem 'stripe' and location from github

        Get details from https://stripe.com/docs/checkout/rails -> home.html.erb

        in config/routes.rb add resources :charges

        delete publishable_key in home.html.erb

  12. Charges controller

        Sign up for a stripe account

        Ensure that the stripe account is on test

        copy the test publishable_api_key -> home.html.erb

        create new charges controller -> app/controllers/charges_controller.rb

        open app/controllers/pages_controller. copy class ChargesController < ApplicationController to charges_controller.rb

        Add the def create method here too

        configure the app.

        create a new initializer -> config/initializers/stripe.rb

  13. Install Figaro

        go to https://github.com/laserlemon/figaro

        add gem and run _bundle install_

        then run bundle exec figaro install

        copy secret_api_key and publishable_api_key to application.yml

        create app/views/charges/

  14. Modify Credit Card Form

        amend home.html.erb

        amend ApplicationController

  15. Purchase last

        run _rails generate model Purchase_
        remove test files
          rm test/fixtures/purchases.yml

        open db/migrate/ file
          amend it

          run rake db:migrate

        create purchases_controller.rb

        amend charges_controller.rb

        amend routes.rb

        create app/views/purchases/show.html.erb

        
