# Login Form Demo

This repository contains a simple web application written in Ruby on Rails.

It has a signup form and login form where you can signup for a new user account and login to an existing user account.

The goal of this kata is to simulate a real world example of how we use Test Driven Development (TDD) on an existing code base. So given a ready made web application, how would you use TDD to drive the introduction of a new feature - in this case, an enhancement to the signup form.

Your facilitators will show you how to use a "Test First" strategy of adding new automated test codes in the test suite (to simulate the new feature), before attempting to build the feature in the leanest way, and then proceed to refactor the code. We hope that you will see how having automated tests helps you in building higher quality code.

If time permits, your facilitators may also introduce you to the idea of refactoring of an existing code base.

---

## Background

The product owner is very happy with the application, but would like some enhancements. People are able to sign up for new accounts, but the ACISO (Agency Chief Information Security Officer) said that some users are able to sign-up with too short a password. Security policy recommends enforcing a longer password length of at least 12 characters to make the application more secure.

### User Story

> As a **User**, <br>
**When** I signup with for a new user account.<br>
**And** I key in a password which is too short.<br>
**Then** I should see an alert telling me my password is too short.

Acceptance Criteria:

- Error alert should be visible when the password is too short.
- Password must be at least 12 characters in length.
- This should be a server-side implementation.
- There should be additional automated test coverage.

---

## Running the application

Open this folder in your terminal app. And run these commands in the terminal. This app assumes you have Ruby 2.6.6 installed.

1. Install dependencies:

    ```
    bundle install
    yarn install
    ```

2. Start the app:

    ```
    bundle exec rails server
    ```

    You can open this url in your browser to view the app: <http://localhost:3000>

3. To run the test:

    ```
    bundle exec rspec
    ```

4. To run the linter:

    ```
    bundle exec rubocop
    ```

5. To fix linting issues:

    ```
    bundle exec rubocop -A
    ```

## Architecture

- **[Ruby on Rails](https://rubyonrails.org/)** - Application framework in Ruby.
- **[ERB](https://en.wikipedia.org/wiki/ERuby)** - Templating engine for displaying the HTML pages.
- **[RSpec](https://rspec.info/)** - Testing framework.
- **[Shoulda Matchers](https://matchers.shoulda.io/)** - Test Assertion library.
- **[SQLite](https://www.sqlite.org/index.html)** - Default database in Rails.
- **[Bootstrap](https://getbootstrap.com/)** - CSS framework for building websites.
- **[RuboCop](https://github.com/rubocop-hq/rubocop)** - Find and fix problems in your Ruby code.

## Routes

1. `GET /`

    This is the home page. The login form is also here.

2. `GET /signup`

    This is the registration form.

3. `POST /signup`

    Sign up for new user account.

4. `POST /users`

    This is how you login to the app. You will need to login with `email` and `password`.

    The default email is `demo@example.com` and password is `demo1234`.

5. `GET /users/welcome`

    Landing page after you have successfully logged in with the correct credentials.

6. `GET /users/logout`

    URL for logging out of the application.
