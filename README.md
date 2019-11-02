# Laravel Vue Starter
> A Laravel-Vue SPA starter project template.

Based on the laravel-vue-starter [here](https://github.com/cretueusebiu/laravel-vue-spa)

## Features

- Laravel 6.0
- Vue + VueRouter + Vuex + VueI18n + ESlint
- Pages with dynamic import and custom layouts
- Login, register, email verification and password reset
- Authentication with JWT
- Socialite integration

## Installation

- Edit `.env` and set your database connection details
- (When installed via git clone or download, run `php artisan key:generate` and `php artisan jwt:secret`)
- `php artisan migrate`
- `yarn install`

## Usage

#### Development

```bash
# build and watch
yarn watch

# serve with hot reloading
yarn hot
```

#### Production

```bash
yarn production
```

## Socialite

This project comes with GitHub as an example for [Laravel Socialite](https://laravel.com/docs/5.8/socialite).

To enable the provider create a new GitHub application and use `https://example.com/api/oauth/github/callback` as the Authorization callback URL.

Edit `.env` and set `GITHUB_CLIENT_ID` and `GITHUB_CLIENT_SECRET` with the keys form your GitHub application.

For other providers you may need to set the appropriate keys in `config/services.php` and redirect url in `OAuthController.php`.

## Email Verification

To enable email verification make sure that your `App\User` model implements the `Illuminate\Contracts\Auth\MustVerifyEmail` contract.
