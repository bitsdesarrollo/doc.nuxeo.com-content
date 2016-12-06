---
title: Document's History
review:
    comment: ''
    date: ''
    status: ok
labels:
    - editing
    - history
    - versioning
toc: true
confluence:
    ajs-parent-page-id: '16092666'
    ajs-parent-page-title: Working in Workspaces
    ajs-space-key: USERDOC58
    ajs-space-name: Nuxeo Platform User Documentation - 5.8
    canonical: Document%27s+History
    canonical_source: 'https://doc.nuxeo.com/display/USERDOC58/Document%27s+History'
    page_id: '16092676'
    shortlink: BI71
    shortlink_source: 'https://doc.nuxeo.com/x/BI71'
    source_link: /display/USERDOC58/Document%27s+History
history:
    - 
        author: Solen Guitter
        date: '2015-08-28 08:48'
        message: ''
        version: '19'
    - 
        author: Solen Guitter
        date: '2014-01-16 15:17'
        message: ''
        version: '18'
    - 
        author: Solen Guitter
        date: '2013-10-22 18:13'
        message: ''
        version: '17'
    - 
        author: Solen Guitter
        date: '2013-02-01 17:05'
        message: ''
        version: '16'
    - 
        author: Solen Guitter
        date: '2013-01-17 18:32'
        message: ''
        version: '15'
    - 
        author: Solen Guitter
        date: '2012-10-02 15:47'
        message: ''
        version: '14'
    - 
        author: Solen Guitter
        date: '2012-06-27 17:59'
        message: Migrated to Confluence 4.0
        version: '13'
    - 
        author: Solen Guitter
        date: '2012-06-27 17:59'
        message: Added TOC and fixed broken link
        version: '12'
    - 
        author: Solen Guitter
        date: '2012-04-03 16:06'
        message: Upated required rights to restore or delete a version
        version: '11'
    - 
        author: Solen Guitter
        date: '2012-01-18 16:38'
        message: Updated screenshots and added details on restoring archived versions
        version: '10'
    - 
        author: Solen Guitter
        date: '2011-11-24 10:06'
        message: ''
        version: '9'
    - 
        author: Solen Guitter
        date: '2011-06-06 11:46'
        message: ''
        version: '8'
    - 
        author: Solen Guitter
        date: '2011-05-31 18:04'
        message: ''
        version: '7'
    - 
        author: Solen Guitter
        date: '2010-12-01 11:21'
        message: ''
        version: '6'
    - 
        author: Solen Guitter
        date: '2010-10-20 10:39'
        message: link update
        version: '5'
    - 
        author: Solen Guitter
        date: '2010-10-20 10:38'
        message: link update
        version: '4'
    - 
        author: Solen Guitter
        date: '2010-09-14 15:44'
        message: fixed broken links
        version: '3'
    - 
        author: Solen Guitter
        date: '2010-05-10 18:39'
        message: fixed broken links
        version: '2'
    - 
        author: Solen Guitter
        date: '2010-04-23 18:11'
        message: ''
        version: '1'

---
&nbsp;

## Viewing a Previous Version of a Document

All users can consult the previous versions of a document.

Every time you modify a document, you can decide to save and archive the state of the document as a new version. Thus the modifications are not erased by future modifications of the document.

The archived versions are listed in the "Archived versions" sub-tab.

![]({{file name='archived-versions.png'}} ?w=650,border=true)

To consult a previous version of a document, click on the **View archived version** button corresponding to the chosen version. The archived version opens.

{{#> callout type='info' heading='Version number 0.0'}}

<div class="message-content">

Draft version 0.0 is not archived. See the page [Editing Content]({{page page='editing-content'}}) for more information about versioning.

</div>

{{/callout}}

Archived versions have few actions available: you can only [create relations]({{page page='relations'}}) from it to another document, [annotate]({{page page='annotations-and-preview'}}) it and subscribe to [notifications]({{page page='alerts'}}).

## Restoring an Older Version of a Document

You need to have "version", "write" or "manage everything" rights to restore a previous version of a document.

Restoring an archived version means making it the current version of the document. The modifications done since that old version are thus not taken into account anymore.

To restore an archived version, click on the **Restore** button corresponding to the chosen version. The document is displayed as it was for the chosen version and has the same archived version's number. The next time it will be modified, its version number will automatically be increased.

![]({{file name='archived-versions-restore.png'}} ?w=650,border=true)

For instance, your document's version is currently 0.3\. When you click on the **Restore** button of the version 0.1, the Summary tab of the document is displayed : the content and metadata are the one of version 0.1, and the version number is 0.1\. When the document is modified, the version number is automatically increased to 0.3+.

## Deleting a Older Version of a Document

You need to have "version", "write" or "manage everything" rights to delete a previous version of a document.

{{#> callout type='warning' }}

Version deletion is a permanent action.

{{/callout}}

**To delete an archived version:**

1.  Check the box corresponding to the version you want to delete.
2.  Click on the **Delete** button below the version list.
    A confirmation window pops up.
3.  Click on the **OK** button to confirm.
    The version is permanently deleted.