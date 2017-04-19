Remove `audit` gem and `audited` on `user.rb` that everything works fine

```
Started POST "/admin/login" for ::1 at 2017-04-19 18:47:34 -0300
Processing by ActiveAdmin::Devise::SessionsController#create as HTML
  Parameters: {"utf8"=>"✓", "authenticity_token"=>"g7f7P3a3RS8hl82MahA32dqXdlCoJjK9TTCWP6DPnjlmYRCUlVPW2fnWicsr8RWeoO7U81/+JdXqM8JLKuNHeg==", "user"=>{"email"=>"admin@example.com", "password"=>"[FILTERED]", "remember_me"=>"0"}, "commit"=>"Login"}
  User Load (0.7ms)  SELECT  `users`.* FROM `users` WHERE `users`.`email` = 'admin@example.com' ORDER BY `users`.`id` ASC LIMIT 1
   (0.3ms)  BEGIN
  SQL (0.6ms)  UPDATE `users` SET `current_sign_in_at` = '2017-04-19 21:47:34', `last_sign_in_at` = '2017-04-19 21:47:00', `sign_in_count` = 5, `updated_at` = '2017-04-19 21:47:34' WHERE `users`.`id` = 1
   (3.0ms)  COMMIT
Can't verify CSRF token authenticity.
Completed 422 Unprocessable Entity in 243ms (ActiveRecord: 4.7ms)



ActionController::InvalidAuthenticityToken (ActionController::InvalidAuthenticityToken):

```
