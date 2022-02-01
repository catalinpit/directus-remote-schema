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

Identify your collection and the permission you want to update. At the top, you can see various icons that represents operations (INSERT, READ, etc).

After that, click on the red symbol and choose "All Access* and you are done.

Alternatively, you can hover the collection name and two options will appear where you can instantly make it public/private.

![Directus Roles and Permissions](https://raw.githubusercontent.com/catalinpit/directus-remote-schema/main/images/directus-set-public-permissions.png)

The collection is now publicly available and you can add Directus as a Remote Schema in Hasura.

## Adding Directus as a Remote Schema

Head over to the Hasura Console, go to the "Remote Schemas" page and click on the "Add" button.

1. Give your Remote Schema a name
2. Add the GraphQL endpoint
3. Click on "Add Remote Schema"

![Hasura Add Remote Schema](https://raw.githubusercontent.com/catalinpit/directus-remote-schema/main/images/hasura-add-remote-schema.png)

After that you are done and you can use the GraphQL API in Hasura!