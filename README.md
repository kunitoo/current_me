# CurrentMe

CurrentMe possesses a current user by a session

## Installation

Add this line to your application's Gemfile:

    gem 'current_me'

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install current_me

## Usage

### Controllers

* When signing, use the `sign_in`

        sign_in user
(※`user` needs to be a user model)

* To Transition to designated page if a user isn't signed in, use the `me!`

        me! signin_path

* When signing out, use the `sign_out`

        def destroy
          sign_out
          redirect_to :root
        end

### Controllers and Views

* If current signed-in user, `me` is available

        Welcome <%= me.name %>

* To verify if a user is signed in, use the `me?`

        <% if me? %>

## Contributing

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request
