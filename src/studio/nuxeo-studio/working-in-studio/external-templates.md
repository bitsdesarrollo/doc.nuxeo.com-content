---
title: External Templates
review:
    comment: ''
    date: ''
    status: ok
labels:
    - content-review-6-0
confluence:
    ajs-parent-page-id: '12911781'
    ajs-parent-page-title: Working in Studio
    ajs-space-key: Studio
    ajs-space-name: Nuxeo Online Services
    canonical: External+Templates
    canonical_source: 'https://doc.nuxeo.com/display/Studio/External+Templates'
    page_id: '8683945'
    shortlink: qYGE
    shortlink_source: 'https://doc.nuxeo.com/x/qYGE'
    source_link: /display/Studio/External+Templates
history:
    - 
        author: Manon Lumeau
        date: '2015-08-07 16:21'
        message: ''
        version: '12'
    - 
        author: Solen Guitter
        date: '2015-01-13 10:54'
        message: ''
        version: '11'
    - 
        author: Solen Guitter
        date: '2015-01-13 10:53'
        message: ''
        version: '10'
    - 
        author: Solen Guitter
        date: '2013-02-26 17:30'
        message: ''
        version: '9'
    - 
        author: Alain Escaffre
        date: '2011-09-18 21:40'
        message: Migrated to Confluence 4.0
        version: '8'
    - 
        author: Alain Escaffre
        date: '2011-09-18 21:40'
        message: ''
        version: '7'
    - 
        author: Alain Escaffre
        date: '2011-09-18 21:24'
        message: ''
        version: '6'
    - 
        author: Alain Escaffre
        date: '2011-09-18 21:23'
        message: ''
        version: '5'
    - 
        author: Alain Escaffre
        date: '2011-09-18 21:21'
        message: ''
        version: '4'
    - 
        author: Alain Escaffre
        date: '2011-09-18 21:16'
        message: ''
        version: '3'
    - 
        author: Alain Escaffre
        date: '2011-09-18 21:13'
        message: ''
        version: '2'
    - 
        author: Alain Escaffre
        date: '2011-09-18 21:11'
        message: ''
        version: '1'

---
Nuxeo Studio includes an Application Templates library composed of Studio projects or samples that you can use as a basis for your own project. This enables you to import new document types, lifecycles, workflows, features in your project as a template that you can edit to adapt it to your project.

To make Nuxeo Studio discovery easier, we automatically import the [Default configuration]({{page space='Studio' page='Default configuration+templates'}}) template that corresponds to your target application when a Studio project is created. You can then see how the configuration is done and start your project from it.

In the Application Templates library, you will find very complex ready-to-use templates for complete function use cases (such as Human resources - Vacation request workflow) or some unitary cases, such as Custom Doc ID generation or Nuxeo School: Sending emails.

For each application template you're displayed some a set of information:

*   **Project version**: The version number of the application template.
*   **Target version**: The version of the Nuxeo Platform and possible add-ons required to install the template.
*   **Import this package**: Click on this button to import the package that you want and follow the instructions. This button is displayed only if your Studio project is configured for a compatible target version of the template.
*   **Details**: Click on this button to be displayed the list of Studio configuration items defined by the template.

![]({{file name='application_templates.png'}} ?w=650,border=true)

For more information about application templates you can see the page [Using Application Templates]({{page page='using-application-templates'}}) and [the detailed documentation for each of them]({{page page='templates-reference'}}).

&nbsp;

* * *