---
title: Add predefined users and groups
review:
    comment: ''
    date: ''
    status: ok
labels:
    - studio-20
    - user-management
    - content-review-6-0
confluence:
    ajs-parent-page-id: '12911810'
    ajs-parent-page-title: Roles & Permissions Section
    ajs-space-key: Studio
    ajs-space-name: Nuxeo Online Services
    canonical: Add+predefined+users+and+groups
    canonical_source: 'https://doc.nuxeo.com/display/Studio/Add+predefined+users+and+groups'
    page_id: '4689311'
    shortlink: n41H
    shortlink_source: 'https://doc.nuxeo.com/x/n41H'
    source_link: /display/Studio/Add+predefined+users+and+groups
history:
    - 
        author: Florent Guillaume
        date: '2012-08-24 15:58'
        message: igrated to Confluence 4.
        version: '7'
    - 
        author: Florent Guillaume
        date: '2012-08-24 15:58'
        message: ''
        version: '6'
    - 
        author: Solen Guitter
        date: '2011-09-05 17:46'
        message: ''
        version: '5'
    - 
        author: Alain Escaffre
        date: '2011-01-14 08:44'
        message: ''
        version: '4'
    - 
        author: Alain Escaffre
        date: '2011-01-14 08:42'
        message: ''
        version: '3'
    - 
        author: Solen Guitter
        date: '2011-01-12 16:36'
        message: ''
        version: '2'
    - 
        author: Solen Guitter
        date: '2011-01-11 18:16'
        message: ''
        version: '1'

---
Some features in Nuxeo products you will configure with Studio are restricted to very specific groups or users. To make sure that users are not blocked by a missing group that the functional administrators would have forgotten to create, Studio enables you to configure users and groups that will automatically be created by the system.
The "members" and "administrators" groups are typically groups created by the system and used for default permissions, for instance. This feature is also very useful when you want to prepare a demo and be sure that you just need to deploy your plugin to have everything ready.

The steps to add a new user or a new group are basically the same.

{{#> panel heading='To add a user or group:'}}

1.  In the left menu, click **Roles and Permissions** and **Users & Groups**.
    *   If users and groups have already been created, the Users tab is displayed with already existing users listed. Jump to step 3 to add new users.
    *   If users and groups haven't been defined yet, a **Create** button is displayed. Continue to step 2 to create default users and groups.
2.  If no user and group have been defined, click on the **Create** button.
    The "Administrator" user and the groups "members" and "administrators" are automatically created by the system. You can now add new default users and groups.
3.  In the Users or Groups tab, click the **Add** button.
4.  In the window that pops up, type the new user's or group's name.
    ![]({{file name='STUDIO-UsersGroups.png'}} ?w=600)
5.  Edit the user's or group properties (see below for more details).
6.  Click **Save**. {{#> callout type='note' }}

    When you deploy your customizations, you will need to empty your database to enable the creation of these users and groups. Until you do so, you will only have the users and groups of a default Nuxeo application.

    {{/callout}} {{#> callout type='warning' }}

    If you choose a Creation Policy of "Always", then at each reload or restart the Studio-defined users and groups will **completely replace** anything you may have changed from Nuxeo. Any updates, additions or removals done from Nuxeo will be lost.

    {{/callout}}

{{/panel}}

**Users properties**

<table><tbody><tr><th colspan="1">

Field

</th><th colspan="1">

Description

</th></tr><tr><td colspan="1">

Name

</td><td colspan="1">

Login of the user. It can only hold alphanumeric characters.

</td></tr><tr><td colspan="1">

Password

</td><td colspan="1">

Type the password of the predefined user.

</td></tr><tr><td colspan="1">

First name

</td><td colspan="1">

Optionally type the first name of the user.

</td></tr><tr><td colspan="1">

Last name

</td><td colspan="1">

Optionally type the last name of the user.

</td></tr><tr><td colspan="1">

Email

</td><td colspan="1">

Optionally type an email address for the user, that will be used for email alerts.

</td></tr><tr><td colspan="1">

Company

</td><td colspan="1">

Optionally fill in the user's company name.

</td></tr><tr><td colspan="1">

Groups

</td><td colspan="1">

Use the > and < arrows to add or remove the user from one of the predefined groups.

</td></tr></tbody></table>

**Groups properties**

<table><tbody><tr><th colspan="1">

Field

</th><th colspan="1">

Description

</th></tr><tr><td colspan="1">

Name

</td><td colspan="1">

The name and ID of the group. It can only hold alphanumeric characters.

</td></tr><tr><td colspan="1">

Description

</td><td colspan="1">

An optional describing what the group is used for.

</td></tr><tr><td colspan="1">

Users

</td><td colspan="1">

Use the > and < arrows to add or remove predefined users from the group by default.

</td></tr></tbody></table>