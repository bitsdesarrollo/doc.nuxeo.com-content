---
title: How to Make Web UI the Default UI
review:
    comment: ''
    date: '2016-12-06'
    status: ok
details:
    howto:
        excerpt: Learn how to make the new Web UI the default UI instead of the JSF UI.
        level: Beginner
        tool: XML Extension
        topics: 'Web UI, JSF UI'
labels:
    - lts2016-ok
    - howto
confluence:
    ajs-parent-page-id: '20517820'
    ajs-parent-page-title: JSF UI How-To Index
    ajs-space-key: NXDOC
    ajs-space-name: Nuxeo Platform Developer Documentation
    canonical: How+to+Make+JSF+UI+the+Default+UI
    canonical_source: 'https://doc.nuxeo.com/display/NXDOC/How+to+Make+JSF+UI+the+Default+UI'
    page_id: '31689315'
    shortlink: Y4rjAQ
    shortlink_source: 'https://doc.nuxeo.com/x/Y4rjAQ'
    source_link: /display/NXDOC/How+to+Make+JSF+UI+the+Default+UI
tree_item_index: 1800
history:
    -
        author: Solen Guitter
        date: '2016-09-05 09:39'
        message: ''
        version: '4'
    -
        author: Solen Guitter
        date: '2016-09-01 09:21'
        message: ''
        version: '3'
    -
        author: Solen Guitter
        date: '2016-09-01 09:20'
        message: ''
        version: '2'
    -
        author: Antoine Taillefer
        date: '2016-09-01 09:15'
        message: ''
        version: '1'

---
On Nuxeo 8.10, in case both _nuxeo-jsf-ui_&nbsp;and _nuxeo-web-ui_ addons are installed, the login page redirects to the JSF UI.
If you want to change this behavior to be redirected to the new Web UI you can add the following XML contribution:

```xml
<extension target="org.nuxeo.ecm.platform.ui.web.auth.service.PluggableAuthenticationService" point="loginScreen">
  <loginScreenConfig>
    <startupPages>
      <startupPage id="web" priority="1000" />
    </startupPages>
  </loginScreenConfig>
</extension>
```

Note that the default `priority`&nbsp;values are:

*   JSF UI (`id="jsf"`): 100
*   Web UI ( `id="web"` ): 10

The highest priority wins.

See [NXP-19992](https://jira.nuxeo.com/browse/NXP-19992)&nbsp;for details.
