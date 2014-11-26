# Article update

To use FreshRSS at its full potential, it needs to grab subscribed feeds new articles. To do so, you have several methods available.

## Automatic update

This is the recommended method since you can forget about it once it is configured.

### With the actualize_script.php script

This method is available only if you have access to the installation server scheduled tasks.

The script is named *actualize_script.php* and is located in the *app* folder. The scheduled task syntax won't be explained here. However, here is [a quick introduction to crontab](http://www.adminschoice.com/crontab-quick-reference/) that might help you.

Here is an example to trigger article update every hour.

```cron
0 * * * * php /path/to/FreshRSS/app/actualize_script.php > /tmp/FreshRSS.log 2>&1
```


### Online cron

If you don't have access to the installation server scheduled task, you can still automate the update process.

To do so, you need to create a scheduled task which need to call a specific URL: https://your.server.net/FreshRSS/p/i/?c=feed&a=actualize (it could be different depending on your installation). Depending on your application authentication method, you need to adapt the scheduled task.

#### No authentication

This is the most straightforward since you have a public instance, there is nothing special to configure:

```cron
0 * * * * curl 'https://your.server.net/FreshRSS/p/i/?c=feed&a=actualize'
```

### Form or Persona authentication

In those cases, if you configure the application to allow anonymous reading, you can also allow anonymous user to update feeds ("Allow anonymous refresh of the articles").

{{:fr:users:anonymous_access.1.png|Configuration de l'accès anonymes}}

The URL used in the previous section becomes accessible and therefore, you can use the same syntax for the scheduled task.

You can also configure an authentication token to grant a special right on the server.

{{:fr:users:token.1.png|Configuration du token}}

The scheduled task syntax to use will be the following:

```cron
0 * * * * curl 'https://your.server.net/FreshRSS/p/i/?c=feed&a=actualize&token=my-token'
```


### HTTP authentication

In that case, the syntax in the two previous section are unusable. It means that you need to provide your credentials to the scheduled task. **Note that this method is highly discouraged since it means that your credentials will be in plain sight!**

```cron
0 * * * * curl -u alice:password123 'https://your.server.net/FreshRSS/p/i/?c=feed&a=actualize'
```

## Manual update

If you can't or don't want to use the automatic methods, you can make it manually. There is two ways, the partial or the complete update.

### Complete update

This update occurs on all feeds. To trigger it, you need to click on the navigation menu update link.

{{ :fr:users:refresh.1.png |Menu de navigation}}

When the update starts, a progress bar appears and changes while feeds are processed.

{{:fr:users:refresh.5.png?nolink|Barre de progression}}

### Partial update

This update occurs on the selected feed only. To trigger it, you need to click on the feed menu update link.

{{:fr:users:refresh.2.png?nolink|Menu du flux}}

