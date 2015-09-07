Theia File Monitor
==================
- A simple php script to monitor when files are changed, erased or added. 
- It uses a simple md5 sum to see if the content of the file has been changed.
- Does not check the timestamps (file last accessed, modified or created).
- Useful for keeping an eye on your files for code injection, or accidental overwrite.

Installation
------------
Just clone the repository and run the script
```shell
php theia-monitor.php --path /var/www/
```

Requirements
------------
- Write permissions on the folder where this scripts runs from

Usage
-----
- Show help screen with all commands
```shell
php theia-monitor.php --help
```

- Show monitored paths
```shell
php theia-monitor.php --show-paths
```

- Show files in path
```shell
php theia-monitor.php --show-files --path /my/path
```

- Monitor files and show the report on screen
```shell
php theia-monitor.php --path /my/path
```

- Monitor files, exlude images and log files (using regular expressions)
```shell
php theia-monitor.php --path /my/path --exclude "(.+\.log)|(access|error)_log|(.+\.(jpe?g|png|gif))"
```

- Monitor files and send the report on email
```shell
php theia-monitor.php --path /my/path --email recipient@example.com --subject "Non-default subject" --from optional-from@example.com --cc "optional-bcc@example.com,email2@example.com"
```

Support
-------
If you find any bugs, open an issue on [GitHub](https://github.com/firewizard/theia-monitor/issues).

Contribution
------------
Any contribution is highly appreciated. Just open a [pull request on GitHub](https://help.github.com/articles/using-pull-requests) with the new feature or fix.

Developer
---------
Cristian Nicolescu
[http://mandagreen.com](http://mandagreen.com)  
[@firewizard](https://twitter.com/firewizard)

License
-------
[MIT License (MIT)](http://opensource.org/licenses/MIT)

