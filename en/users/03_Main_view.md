# Normal view

**TODO**

# Global view

**TODO**

# Reader view

**TODO**

# Refreshing feeds

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

# Filtering articles

While the number of articles stored by FreshRSS increase, it is important to have efficient filters to display only a subset of the articles. There is several methods with different criterion. Most of the time, those methods can be combined.

##By category

It is the easiest method. The only thing to do is clicking on the category title in the side panel. There is two special categories on top of that panel:
  * *Main feed* which displays only articles from feeds marked as available in that category
  * *Favorites* which displays only articles marked as favorites

##By feed

There is several methods to filter articles by feed:
  * by clicking the feed title in the side panel
  * by clicking the feed title in the article details
  * by filtering in the feed options from the side panel
  * by filtering in the feed configuration

##By status

Each article has two attributes which can be combined. The first attribute indicates if the article was read or not. The second attribute indicates if the article was marked as favorite or not.

With version 0.7, attribute filters are available in the article display drop-down list. With this version, it is not possible to combine those filters. For instance, it is not possible to display only read and favorite articles.

Starting with version 0.8, all attribute filters are visible as toggle icons. They can be combined. As any combination is possible, some have the same result. For instance, the result for all filters selected is the same as no filter selected.

By default, this filter displays only unread articles

##By content

It is possible to filter articles by their content by inputting a string in the search field.

##By keyword

Version 0.7.x introduced the support of keyword filters. They must be used in the search field used for the content filtering.

  * by author:
```
author:<name>
```
  * by title:
```
intitle:<title>
```
  * by URL:
```
inurl:<url>
```

Be aware that there is no space between the keyword and the value.
Note also that keywords can not be combined.

Version 0.8.x introduced a new keyword to search by dates. The format used is the [ISO 8601](http://en.wikipedia.org/wiki/ISO_8601#Time_intervals) format.
```
date:<date>
```

It is also possible to combine keywords to have a very sharp filter.

# Searching articles

**TODO**
