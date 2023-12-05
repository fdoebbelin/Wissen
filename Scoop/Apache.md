## Apache with PHP

Install PHP and Apache:

```
scoop install php apache
```

Register the PHP handler with Apache:

```
$apache = scoop which httpd
$conf = "$(split-path $apache)/../conf/httpd.conf"
$php = scoop which php
$phpmodule = "$(split-path $php -resolve)\php8apache2_4.dll"
$lines = gc $conf
$phpmodule = $phpmodule -replace '\\', '/'
$new = @"
LoadModule php_module '$phpmodule'
AddHandler application/x-httpd-php .php
PHPIniDir `"$(split-path $phpmodule)`"
"@
out-file $conf -append -encoding utf8
```

**To start Apache on the command line**, run:

```
httpd
```

Apache will continue running until you press `Ctrl-C` to terminate it.

If you open `http://localhost` in your browser, you should see a page saying that “It works!”.

## [#](https://scoop-docs.vercel.app/docs/guides/Apache-with-PHP.html#the-document-root-directory) The document root directory

Scoop configures Apache to serve web pages from the `htdocs` directory inside the Scoop install directory.

You can get to this directory by running:

```
pushd "\$(scoop which httpd | split-path)\..\htdocs"
```

If you would like to serve documents from somewhere else, you need to change the DocumentRoot inside the `conf/httpd.conf` file. You can find `httpd.conf` at

```
"$(scoop which httpd | split-path)\..\conf\httpd.conf"
```

## [#](https://scoop-docs.vercel.app/docs/guides/Apache-with-PHP.html#installing-apache-as-a-service) Installing Apache as a service

Run:

```
sudo httpd -k install -n apache
sudo net start apache
```

If you don't have `sudo`, you can install it with `scoop install sudo`.

To uninstall the Apache service

```
sudo net stop apache
sudo httpd -k uninstall -n apache
```

For more information, see [Using Apache HTTP Server on Windows](https://httpd.apache.org/docs/current/platform/windows.html)

`LoadModule php5_module "D:/php/php5apache2_4.dll"`
`AddHandler application/x-httpd-php .php`
`# configure the path to php.ini`
`PHPIniDir "D:/php"`

In addition to above, go ahead and add index.php to DirectoryIndex variable in following manner:

```
<IfModule dir_module>
    DirectoryIndex index.php index.html
</IfModule>
```
