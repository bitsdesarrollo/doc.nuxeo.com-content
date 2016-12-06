---
title: Email Folders
review:
    comment: ''
    date: ''
    status: ok
labels:
    - dm-document
toc: true
confluence:
    ajs-parent-page-id: '16092666'
    ajs-parent-page-title: Working in Workspaces
    ajs-space-key: USERDOC58
    ajs-space-name: Nuxeo Platform User Documentation - 5.8
    canonical: Email+Folders
    canonical_source: 'https://doc.nuxeo.com/display/USERDOC58/Email+Folders'
    page_id: '16092631'
    shortlink: '1431'
    shortlink_source: 'https://doc.nuxeo.com/x/1431'
    source_link: /display/USERDOC58/Email+Folders
history:
    - 
        author: Solen Guitter
        date: '2015-08-28 09:02'
        message: ''
        version: '23'
    - 
        author: Solen Guitter
        date: '2014-06-11 15:15'
        message: ''
        version: '22'
    - 
        author: Solen Guitter
        date: '2013-10-22 18:19'
        message: ''
        version: '21'
    - 
        author: Solen Guitter
        date: '2013-09-30 17:12'
        message: ''
        version: '20'
    - 
        author: Solen Guitter
        date: '2012-07-24 11:42'
        message: Migrated to Confluence 4.0
        version: '19'
    - 
        author: Solen Guitter
        date: '2012-07-24 11:42'
        message: Added related pages
        version: '18'
    - 
        author: Solen Guitter
        date: '2012-07-24 11:38'
        message: Added related pages
        version: '17'
    - 
        author: Solen Guitter
        date: '2012-07-03 17:46'
        message: Added related pages
        version: '16'
    - 
        author: Solen Guitter
        date: '2012-05-30 17:01'
        message: Added TOC
        version: '15'
    - 
        author: Solen Guitter
        date: '2011-11-24 10:44'
        message: ''
        version: '14'
    - 
        author: Solen Guitter
        date: '2011-11-09 09:48'
        message: ''
        version: '13'
    - 
        author: Solen Guitter
        date: '2011-11-08 17:09'
        message: ''
        version: '12'
    - 
        author: Solen Guitter
        date: '2011-06-06 14:55'
        message: ''
        version: '11'
    - 
        author: Solen Guitter
        date: '2010-10-20 10:41'
        message: ''
        version: '10'
    - 
        author: Solen Guitter
        date: '2010-10-20 10:39'
        message: ''
        version: '9'
    - 
        author: Solen Guitter
        date: '2010-09-23 17:01'
        message: ''
        version: '8'
    - 
        author: Solen Guitter
        date: '2010-09-23 17:00'
        message: added screenshots
        version: '7'
    - 
        author: Solen Guitter
        date: '2010-09-23 16:31'
        message: ''
        version: '6'
    - 
        author: Solen Guitter
        date: '2010-09-23 14:59'
        message: ''
        version: '5'
    - 
        author: Solen Guitter
        date: '2010-09-21 18:25'
        message: ''
        version: '4'
    - 
        author: Solen Guitter
        date: '2010-09-21 18:19'
        message: ''
        version: '3'
    - 
        author: Solen Guitter
        date: '2010-09-21 18:07'
        message: ''
        version: '2'
    - 
        author: Solen Guitter
        date: '2010-04-14 11:31'
        message: ''
        version: '1'

---
&nbsp;

{{#> callout type='note' }}

The emails imported in the email folder cannot be modified in Nuxeo.

{{/callout}}

## Creating an Email Folder

**To create an email folder**

1.  In a workspace, click on the **New** button.
2.  In the modal window displayed, click on **Email folder**
    The email folder creation form is displayed.
3.  Fill in the creation form (see parameters below) and click on the **OK** button.
    The **Content** tab of the email folder is displayed.
    ![]({{file name='DM-emailFolder-created.png'}} ?w=650,border=true)
    You can now fetch emails.

**Email folder parameters**

<div class="table-scroll"><table class="hover"><tbody><tr><th colspan="1">

Field

</th><th colspan="1">

Description

</th></tr><tr><td colspan="1">

Title

</td><td colspan="1">

Name of your email folder

</td></tr><tr><td colspan="1">

Email

</td><td colspan="1">

Email address of the account from which the emails will be fetched.

</td></tr><tr><td colspan="1">

Password

</td><td colspan="1">

Password of the email account from which the emails will be fetched.

</td></tr><tr><td colspan="1">

Protocol

</td><td colspan="1">

Select the receive protocol used for the email account.

</td></tr><tr><td colspan="1">

Host

</td><td colspan="1">

Type the name of the host of the email account.

</td></tr><tr><td colspan="1">

Port

</td><td colspan="1">

Type the port number.\ Default value is 993, which should be ok in most cases. Check with your administrator if this value should be changed.

</td></tr><tr><td colspan="1">

Socket factory fallback

</td><td colspan="1">

Default value is set to "Yes". This parameter sets the behaviour in case the socket used to connect the Nuxeo server to the email server fails to be created using the implemented socket factory.

</td></tr><tr><td colspan="1">

Socket factory port

</td><td colspan="1">

Port used to connect the Nuxeo server to the email server. Default value is set to 993.

</td></tr><tr><td colspan="1">

Start TLS (IMAP)

</td><td colspan="1">

Default value is set to "Yes" to secure exchanges with the email server.

</td></tr><tr><td colspan="1">

SSL protocols (IMAP)

</td><td colspan="1">

Default value is "SSL". You can add other protocols, separated by whitespace.

</td></tr><tr><td colspan="1">

Limit of new fetched emails

</td><td colspan="1">

Indicate the maximum number of emails to be fetched at the same time.

</td></tr></tbody></table></div>

The actions available on an email folder are:

*   Edit the folder (see parameters above),
*   Subscribe to [alerts]({{page page='alerts'}}),
*   [Manage the access]({{page page='managing-access-rights'}}) to the folder,
*   [Manage the trash]({{page page='managing-deleted-documents'}}) of the folder.

## Fetching Emails

**To fetch emails:**

1.  In your email client, mark the emails you want to fetch as unread.
2.  In Nuxeo, open the email folder.
    The **Content** tab is displayed.
3.  Click on the **Check email** button.
    The unread emails are imported in the email folders.
    ![]({{file name='DM-emailFolder-content.png'}} ?w=650,border=true)
4.  To open a mail, click on its subject
    ![]({{file name='DM-emailFolder-summary.png'}} ?w=650,border=true)

Emails cannot be edited, but you can [comment]({{page page='comments'}}) and [annotate]({{page page='annotations-and-preview'}}) them, [link]({{page page='relations'}}) them to other documents and [follow the email folder's activity]({{page page='alerts'}}).

&nbsp;