#ruby #rails
# Default directory structure
Example from https://github.com/JetBrains/sample_rails_app:
```
sample_rails_app
├── app
│   ├── assets
│   │   ├── config
│   │   │   └── manifest.js
│   │   ├── images
│   │   └── stylesheets
│   ├── channels
│   │   └── application_cable
│   │       ├── channel.rb
│   │       └── connection.rb
│   ├── controllers
│   │   ├── static_pages_controller.rb
│   │   └── users_controller.rb
│   ├── helpers
│   │   ├── static_pages_helper.rb
│   │   └── users_helper.rb
│   ├── javascript
│   │   ├── channels
│   │   │   ├── consumer.js
│   │   │   └── index.js
│   │   └── packs
│   │       └── application.js
│   ├── jobs
│   │   └── application_job.rb
│   ├── mailers
│   │   ├── application_mailer.rb
│   ├── models
│   │   ├── application_record.rb
│   │   └── user.rb
│   └── views
│       ├── layouts
│       │   ├── application.html.erb
│       │   ├── _footer.html.erb
│       │   ├── _header.html.erb
│       │   ├── mailer.html.erb
│       │   ├── mailer.text.erb
│       │   └── _shim.html.erb
│       ├── microposts
│       │   └── _micropost.html.erb
│       ├── password_resets
│       │   ├── edit.html.erb
│       │   └── new.html.erb
├── babel.config.js
├── bin
│   ├── bundle
│   ├── rails
│   ├── rake
│   ├── setup
│   ├── spring
│   ├── webpack
│   ├── webpack-dev-server
│   └── yarn
├── config
│   ├── application.rb
│   ├── boot.rb
│   ├── cable.yml
│   ├── credentials.yml.enc
│   ├── database.yml
│   ├── environment.rb
│   ├── environments
│   │   ├── development.rb
│   │   ├── production.rb
│   │   └── test.rb
│   ├── initializers
│   │   ├── application_controller_renderer.rb
│   │   ├── assets.rb
│   │   ├── backtrace_silencers.rb
│   │   ├── content_security_policy.rb
│   │   ├── cookies_serializer.rb
│   │   ├── filter_parameter_logging.rb
│   │   ├── inflections.rb
│   │   ├── mime_types.rb
│   │   └── wrap_parameters.rb
│   ├── locales
│   │   ├── de.yml
│   │   ├── en.yml
│   │   └── es.yml
│   ├── puma.rb
│   ├── routes.rb
│   ├── spring.rb
│   ├── storage.yml
│   ├── webpack
│   │   ├── development.js
│   │   ├── environment.js
│   │   ├── production.js
│   │   └── test.js
│   └── webpacker.yml
├── config.ru
├── db
│   ├── migrate
│   │   ├── 20190822013911_create_users.rb
│   ├── schema.rb
│   └── seeds.rb
├── docker-compose.yml
├── Dockerfile
├── Gemfile
├── Gemfile.lock
├── Guardfile
├── HELP.md
├── lib
│   ├── assets
│   └── tasks
│       └── my_task.rake
├── LICENSE.md
├── log
├── package.json
├── postcss.config.js
├── Procfile
├── public
│   ├── 404.html
│   ├── 422.html
│   ├── 500.html
│   ├── apple-touch-icon.png
│   ├── apple-touch-icon-precomposed.png
│   ├── favicon.ico
│   └── robots.txt
├── Rakefile
├── README.md
├── spec
│   ├── factories.rb
│   ├── models
│   │   └── user_spec.rb
│   ├── rails_helper.rb
│   ├── spec_helper.rb
│   └── support
│       └── factory_bot.rb
├── storage
├── test
│   ├── application_system_test_case.rb
│   ├── channels
│   │   └── application_cable
│   │       └── connection_test.rb
│   ├── controllers
│   ├── fixtures
│   │   ├── files
│   │   ├── microposts.yml
│   ├── helpers
│   ├── integration
│   ├── mailers
│   │   ├── previews
│   │   │   └── user_mailer_preview.rb
│   │   └── user_mailer_test.rb
│   ├── models
│   ├── system
│   └── test_helper.rb
├── tmp
├── vendor
└── yarn.lock
```