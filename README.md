# directus-remote-schema

Directus is an open-source Headless CMS with the flexibility and power of a Data API. It allows managing both content and raw data, in any new or existing SQL database — keeping all your data pure, organized and portable, end-to-end.

## Add Directus as a Remote Schema

After creating the Directus application, you can access the GraphQL API endpoint as follows:

```
https://<your-project-name>.directus.app/graphql
```

It's important to note that all data is accesible only to authenticated users. There are three ways to access data:
* make your data public
* use JWTs
* use static tokens (set for each user) which do not expire

### Make Data Public

There are scenarios where your data can be made publicly available. If that's your case, go to the **Roles & Permissions** page in your project's dashboard.

Once you are there, click on the **Public** role.

![Directus Roles and Permissions](https://raw.githubusercontent.com/catalinpit/directus-remote-schema/main/images/directus-roles-permissions.png)

A new page opens where you can set the permissions for all your collections.

![Directus Roles and Permissions](https://raw.githubusercontent.com/catalinpit/directus-remote-schema/main/images/directus-set-public-permissions.png)