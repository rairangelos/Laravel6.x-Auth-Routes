# Laravel 6.x Auth Routes
**A summarized scope of the auth routes set in the new version of Laravel 6**

## Auth Routes :+1:
- [x] File path: vendo/laravel/framework/src/Illuminate/routing/Router.php


> **Authentication Routes...**
- Route::get('login', 'Auth\LoginController@showLoginForm')->name('login');
- Route::post('login', 'Auth\LoginController@login');
- Route::post('logout', 'Auth\LoginController@logout')->name('logout');

> **Registration Routes...**
- Route::get('register', 'Auth\RegisterController@showRegistrationForm')->name('register');
- Route::post('register', 'Auth\RegisterController@register');

> **Register the typical reset password routes for an application.**
- Route::get('password/reset', 'Auth\ForgotPasswordController@showLinkRequestForm')->name('password.request');
- Route::post('password/email', 'Auth\ForgotPasswordController@sendResetLinkEmail')->name('password.email');
- Route::get('password/reset/{token}', 'Auth\ResetPasswordController@showResetForm')->name('password.reset');
- Route::post('password/reset', 'Auth\ResetPasswordController@reset')->name('password.update');

> **Register the typical confirm password routes for an application.**
- Route::get('password/confirm', 'Auth\ConfirmPasswordController@showConfirmForm')->name('password.confirm');
- Route::post('password/confirm', 'Auth\ConfirmPasswordController@confirm');

> **Register the typical email verification routes for an application.**
- Route::get('email/verify', 'Auth\VerificationController@show')->name('verification.notice');
- Route::get('email/verify/{id}/{hash}', 'Auth\VerificationController@verify')->name('verification.verify');
- Route::post('email/resend', 'Auth\VerificationController@resend')->name('verification.resend');


## This content aim to give assist to the people who need the routes splitted!
# I hope you enjoy!

## Contributing
Thank you for considering contributing to the Laravel framework! The contribution guide can be found in the [Laravel documentation](https://laravel.com/docs/contributions).

## Security Vulnerabilities
If you discover a security vulnerability within Laravel, please send an e-mail to Taylor Otwell via [taylor@laravel.com](mailto:taylor@laravel.com). All security vulnerabilities will be promptly addressed.

## License
The Laravel framework is open-source software licensed under the [MIT license](https://opensource.org/licenses/MIT).

