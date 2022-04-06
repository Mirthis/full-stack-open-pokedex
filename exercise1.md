Ruby on Rails

- Pipeline steps

  - build, lint and test
    - install OS and service dependencies (i.e.: postgres, redis)
    - install ruby
    - innstall yarn
    - install bundler (gem install bundler)
    - install ruby gems via bundler (bundle install)
    - create database (bundle exec rake db:create)
    - run migrations (bundle exec rake db:migrate)
    - check code with rubocop
    - perform security code scan with brakeman
    - run rspec test - unit, integration, e2e (bundle exec rspec .)
  - deployment
    - push code to heroku (this will trigger install of all the required depedencies)
    - run db creation and migration on heroku (this need to be done manually as not covered by previous step)

- Other CI/CD tools

  - GitLab
  - Azure DevOps
  - Semaphore
  - CircleCI
  - CodeShip

- Cloud based as the setup is farily straightforward, execution is generally fast (it may not be if number of integration and e2e tests is high), and used tools are mature and will unlikely require out of the ordinary customisation. As the application growt and things get more complicated, this may need to be re-assesd, but I wouldn't move to a hosted solution unless there's any major challlenge in executing the pipeline on cloud or cost become prohibitive.
