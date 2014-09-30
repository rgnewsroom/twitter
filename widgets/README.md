## Categories

At this time (June, 2013), there're four types of [Twitter widgets](https://dev.twitter.com/docs/embedded-timelines):

1. User timeline
1. Favorites
1. List
1. Search

## Javascript

The twitter widget HTML requires the below Javascript to run:

```js
<script>!function(d,s,id){var js,fjs=d.getElementsByTagName(s)[0],p=/^http:/.test(d.location)?'http':'https';if(!d.getElementById(id)){js=d.createElement(s);js.id=id;js.src=p+"://platform.twitter.com/widgets.js";fjs.parentNode.insertBefore(js,fjs);}}(document,"script","twitter-wjs");</script>
```

**IMPORTANT:** Because we use Twitter widgets on a regular basis, I've included a variation of the above Javascript into our templates. This means that **you only need to insert the HTML in order to get a Twitter widget to work on any of our pages**.

## Example markup

At this time, there's one widget (with a label of **[Tweets by The Register-Guard (@registerguard)](https://twitter.com/settings/widgets)**) which can be used for all of our widget needs ([except for "search" widgets](https://github.com/registerguard/registerguard.github.com/wiki/Twitter-timeline-widget-guide#search)).

To view the default widget markup, and see examples of how to modify the code, [check out the demo page](http://registerguard.github.io/bulldog/build/files/test/twitter-widgets.html).

Note that the value of `data-widget-id` is the same for all widgets **except** for the "search" (see below).

**Important:** It is required to have a `twitter-timeline` class.

## Attributes

As shown on the demo page, the default widget code can be modified, through the use of HTML attributes, to show different things based on your needs.

### Standard attributes:

Attribute | Value
--: | :--
`href` | URI to corresponding, appropriate location in case the widget is temporarily unavailable
`width` | Default width is `520` pixels.
`height` | Default height is `600` pixels.
`data-theme` | `light`
`data-link-color` | `#cc0000`
`data-chrome` | `noheader nofooter noborders noscrollbar transparent`
`data-border-color` | `#cc0000`
`lang` | `en-US`
`data-tweet-limit` | `5`
`data-related` | `benward, endform`
`aria-polite` | `polite`
`data-dnt` | Set to `true` to [opt-out of Twitter tailoring](https://support.twitter.com/articles/20169421).

### Overrides:

Depending on your needs, use the below attributes to override the default widget behavior.

#### User:

Attribute | Value
--: | :--
`data-screen-name` | `rgsports`
`data-user-id` | `12345`
`data-show-replies` | `true`

#### Favorites:

Attribute | Value
--: | :--
`data-favorites-screen-name` | `rgsports`
`data-favorites-user-id` | `12345`

#### List:

Attribute | Value
--: | :--
`data-list-owner-screen-name` | `registerguard`
`data-list-owner-id` | `12345`
`data-list-id` | `12345`
`data-list-slug` | `rg-march-madness`

#### Search:

At the present time, it is not possible to override search queries. :(
