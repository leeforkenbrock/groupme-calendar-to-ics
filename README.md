# GroupMe Calendar to ICS

Turn your GroupMe event calendar into an ICS feed (for Google Calendar, Apple Calendar, Outlook, etc.).

[![Deploy](https://www.herokucdn.com/deploy/button.png)](https://heroku.com/deploy?template=https://github.com/leeforkenbrock/groupme-calendar-to-ics)

## Deploying

When you set up this app, you'll be required to configure five environment variables:

 * `GROUPME_GROUP_ID` - The ID for the GroupMe group.  This can be found on the webapp (https://web.groupme.com) under the Settings option for your group.
 * `GROUPME_API_KEY` - A [GroupMe Developer Access Token](https://dev.groupme.com/docs/v3) for a user in the GroupMe group.
 * `CACHE_DURATION` - The duration for which the GroupMe calendar is cached.  `0` will disable caching.
 * `GROUPME_CALENDAR_TIMEZONE` - Timezone of the calendar events.  See https://en.wikipedia.org/wiki/List_of_tz_database_time_zones for list. Default is `America/Los_Angeles`
 * `GROUPME_STATIC_NAME` - *(Optional)* A static name for the group.  This will lock a name for the calendar, even if the group decides to change their name.
 * `GROUPME_PROXY_URL` - *(Optional)* A proxy URL to provide for the calendar.ics.


### Default Settings

 * **Cache Rate** - By default, the GroupMe calendar is refreshed and cached by one request every 60 minutes.  This is designed to help rate limit GroupMe API requests.  The caching rate can be modified or disabled by setting it to `0`.
