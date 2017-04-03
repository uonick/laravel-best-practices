# Laravel : The Right Way (Best Practices)

It would be wrong to call any PHP framework the best one, because different frameworks have various advantages. Usually, a PHP developer chooses a particular framework in accordance with the requirements defined in the project. But trust me, I picked up **Laravel** and I totally love it now.

Speaking about **Laravel,** it is simple and comfortable to use, suitable to start with writing the production code, and gives a great boost to a development process. One thing that I love about **Laravel** is that it’s built using the best practices used in programming available in the current times.

What I personally prefer is to always stick to **Laravel**’s recommended Code Base structure, you can do it the alternative way but it could lead you to some issues later on.

Here are some simple things worth having in mind when developing in **Laravel**:

* Try to make use of your **.env** file to the max you can.
* **Don’t Hack Core**. Do not edit the files in the vendor folders, extend the functions instead. **Extension over Modification**.
* Don’t create tables or index directly via PHPMyAdmin or console. Use **Database Migration** to create table, add/alter any fields, and commit those to Git repository.
* Don’t insert fake values directly into the database for testing purposes. Create **Seeder** files to populate your database.
* Prefer to use **Artisan CLI** more than manually creating stuff, it’ll fasten up your productivity.
* Make sure to boost performance using some artisan commands:
   * `php artisan route:cache`
   * `php artisan config:cache`  
   * `php artisan optimize --force`
 
* Try not to write closures into your **routes/web.php** file, instead move them to your controller.
* Be careful with the naming conventions when creating custom classes and functions, especially with your **Models**. **Laravel** works on a principle such that, for a table named **users**, it would expect it’s model name to be **User**.
* Try to make [Validation Requests](https://laravel.com/docs/master/validation#form-request-validation) separately for each request.
* Although PHP has a class named DateTime to help you when reading, writing, comparing or calculating with date and time. It is recommended that you use the **Carbon Library** for dealing with dates.
* Always keep yourself updated with the latest version, **Laravel** is updating real fast, so keep up the pace.
* Always use **gulp, laravel-mix** for compiling your **scripts** and **sass** into minified version for better performance, **Laravel** did the basic housekeeping for you.

Feel free to add more to the list

[original](https://medium.com/@adebsalert/laravel-the-right-way-best-practices-2346cd6c5d89)
