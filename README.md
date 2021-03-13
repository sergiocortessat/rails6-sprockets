# Dependencies
  - Ruby 3.0

# Configuration
1. Use the template and make sure to **uncheck** "Include all branches"
1. Clone the repository to the local machine
1. Initialize git-flow in all local machines with `git flow init`
    1. Set production branch: `main`
    1. Set development branch: `development`
    1. Set the rest of the options as defaults
    1. Initialize a new feature branch. You can call it `setup-template`
1. Run `bundle update` to install the latest version of the gems for the project
1. Reinstall and setup the required packages by running `bundle exec bin/setup`
1. Generate the Rails credentials for the project: `EDITOR=true bundle exec rails credentials:edit`
1. Change the name of the project. Use the commit [324932f](../../commit/324932fbc5e055a3f40dbe2a565ce663f85235d7) as reference
1. Also, do not forget to change the name and version from the `package.json` file
1. Execute the Rubocop command, so the linter's workflow won't fail: `bundle exec rubocop -A`
1. Add and commit all your changes
1. Finalize your feature branch and merge your changes
1. Everything should be ready to start working!

# Code style
This template uses Rubocop for enforcing the code style. In the root path, there are 2 Rubocop configurations. The recommended default is for all new Rails projects. It uses the official and latest cops for the core components and Rails itself.

The alternative version is unmaintained and therefore not recommended. Besides being unmaintained, it disables, changes, and enables cops that conflict with the default and recommended cops. Microverse projects have to use them despite the official recommendation.

# Notes before deploying
1. Change the hostname for devise when deploying to production, check the files inside `config/environments`

> **Note**: all packages already set up, this includes: Devise, RSpec, Capybara, Factory Bot, Rubocop, GitHub Workflow, Faker and it's ready to deploy to Heroku. Start to work with the models, views, and controllers. Note that you'll need to use the correct generators (i.e. `bundle exec rails generate devise User`).
>
> **Note**: The development/test version will use SQLite3, but the deployed version will use PostgreSQL. The bundle command will install the `pg` gem anyway, and if it fails to set it up, install PostgreSQL even if never used or configured.
