httpstatusdogs-nginx
====================

Nginx conf to use [httpstatusdogs.com](http://httpstatusdogs.com) images as nginx error pages

## Usage

  1. Create a directory to put the images
  2. Use the bash commands in `codes.conf` to download the images and generate the error pages
  3. Save `codes.conf` somewhere in your nginx includes directory
  4. Include `codes.conf` in any of your nginx server blocks:

     `include NGINX_INCLUDES_DIR/statusdogs/codes.conf;`
  5. Reload nginx
  6. Share and enjoy :)

## Example

```
server {
  root /var/www/test;
  server_name test.dev;
  listen 80;
  index index.html;
  
  include /usr/local/nginx/includes/statusdogs/codes.conf;
}
```

## Credits

Huge thanks to [Mike Lee](https://twitter.com/mikeleeorg) for putting together the awesome [httpstatusdogs.com](http://httpstatusdogs.com)
  
