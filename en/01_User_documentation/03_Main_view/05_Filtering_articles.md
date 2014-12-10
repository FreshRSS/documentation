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
