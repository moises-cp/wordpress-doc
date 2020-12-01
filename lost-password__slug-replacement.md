# Replace Lost Password URL Slug

To replace/rewrite the Lost Password URL when the user clicks on `Lost Password?` 

- Add the lost password filter to WordPress
  - Copy the code provided below and paste it on the theme `functions.php` file
- Modify the filter to your needs
  - On the line that says `return site_url()`, replace `/password-reset/` with the slug that will be use for directing the user to the `Lost Password` form.
- Test it
  - Go to the login form of your website and click on `Lost Password?`
    - You should be directed to the new URL and you should be able to see the `Get New Password` form.

<br>

```php
/**
 *  Theme functions.php
 */

add_filter( 'lostpassword_url',  'my_lostpassword_url', 10, 0 );
function my_lostpassword_url() {
    return site_url('/password-reset/');
}
```

