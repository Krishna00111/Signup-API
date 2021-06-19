# Signup-API

1) Login API
2)Register API
3)Details API


2. Install Laravel : composer create-project --prefer-dist laravel/laravel blog #command

3. Installing Package : composer require laravel/passport

4. Add service provider : config/app.php
'providers' =>[
Laravel\Passport\PassportServiceProvider::class,
],

5. Step 3: Run Migration and Install
After Passport service provider registers, we require to run the migration command, after run migration command you will get several new tables in the database. So, let’s run below command:
php artisan migrate
Next, we need to install a passport using the command, 

Using passport:install command, it will create token keys for security. So let’s run below command:
php artisan passport:install

6. In model, we added HasApiTokens class.
In auth.php, we added API auth configuration.

7.Step 5: Create API Route
In this step, we will create API routes. Laravel provides api.php file for write web services route. So, let’s add a new route on that file.

8.Step 6: Create the Controller
In the last step we have to create a new controller and three API method, So first create a new directory “API” on Controllers folder. So let’s create UserController and put bellow code:

9.Now we are ready to run our example so run below command to quick run:
php artisan serve

10. Login API:
Now, we can simple test by rest client tools, So I test it and you can see below screenshot for login API.

![1_ftAjiGUA-fbEKTcPBMzuAw](https://user-images.githubusercontent.com/42055861/122641921-d0158b00-d125-11eb-870b-d32c72628bab.png)

11. Validation of Register API:
Validation is the most important aspect while designing an application. It validates the incoming data. By default, the base controller class uses a ValidatesRequests trait which provides a convenient method to validate incoming HTTP requests with a variety of powerful validation rules.
Laravel Provide very strong validator class when you build API with laravel then use ValidatesRequests trait for validating your request I define Validator class in register function

![1_8aRvHuCD4kvSvGWzxgx16g](https://user-images.githubusercontent.com/42055861/122642011-09e69180-d126-11eb-9503-bf40f4e4f4a6.png)

12.Register API:
![1_oh9uu9GJceFfEbclKLO29g](https://user-images.githubusercontent.com/42055861/122642073-2682c980-d126-11eb-8bec-5dac86f61185.png)


13.Now, we will test details API, In this api, you have to set two headers as listed below:
‘headers’ => [
‘Accept’ => ‘application/json’,
‘Authorization’ => ‘Bearer ‘.$accessToken,
]
So, make sure above header, otherwise, you can not get user details.

14. Details API:

![1_oV63bg2V0W1x00eMhucOpQ](https://user-images.githubusercontent.com/42055861/122642102-47e3b580-d126-11eb-8af7-2927629dd033.png)


Through Laravel Application Development, You can able to develop your web application more user-friendly design, secure, scalable and feature-rich that can fulfill your requirement which will help you meet your business goals and take your business to the next level.


