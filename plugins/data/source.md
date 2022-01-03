# What's a collection source in WeWeb?

A collection source represents some data that is added to WeWeb from an external tool.

It can come from many tools (like Airtable or an API) and be filtered or sorted the way you want.

You can add a collection using 3 different modes:

### Static: 
- Useful when you need SEO and if you don’t have much data,
- All the data are pre-rendered with the page, so it works without JavaScript. Google will have them with the first request
- You can use no-code filters (but NOT dynamic filters with variables)
- You can use Postgres filters
- You need to republish if the data change. Manually or with hooks
### Dynamic:
- Useful when you have your own API or if you use a tool designed for production requests
- The request is done directly to the source when the page loads
- You don’t need to republish when the data change
### Cached:
- Useful when your data is somewhere with API limits like Airtable or Google sheets
- The request is done to a dedicated database where we have copied the data from the source.
- You can use no-code filters (and variables to create dynamic filters)
- You can use Postgres filters
- You need to update the cache when the data change. You can do it with weweb workflows, with hooks or manually
