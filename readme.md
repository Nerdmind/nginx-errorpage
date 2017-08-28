# Errorpage customization for nginx HTTP server
This package configures your nginx HTTP server with custom error pages.

## SSI variables
The following variables are defined within each `xxx.shtml` file within the `customization/errorpage/` directory:

* `ERRORPAGE_CODE`: This variable contains the HTTP status code for the current error or information page.
* `ERRORPAGE_TEXT`: This variable contains the description of the HTTP status code defined with `ERRORPAGE_CODE`.

## Installation
All files and directories provided in this package are relative to the `/etc/nginx/` install directory (if your nginx is installed somewhere else, you have to change the paths). To activate the configuration, just include the `errorpage.conf` in each virtual host within the `server {}` or `location {}` block and reload nginx:

	include /etc/nginx/snippets/errorpage.conf;