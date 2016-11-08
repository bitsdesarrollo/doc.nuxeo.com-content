---
title: How to Complete a Workflow Task Programmatically
review:
    comment: ''
    date: ''
    status: ok
labels:
    - workflow
    - workflow-task
confluence:
    ajs-parent-page-id: '17334536'
    ajs-parent-page-title: Workflow How-Tos
    ajs-space-key: NXDOC58
    ajs-space-name: 'Nuxeo Platform Developer Documentation - 5.8 '
    canonical: How+to+Complete+a+Workflow+Task+Programmatically
    canonical_source: >-
        https://doc.nuxeo.com/display/NXDOC58/How+to+Complete+a+Workflow+Task+Programmatically
    page_id: '17334507'
    shortlink: 64AIAQ
    shortlink_source: 'https://doc.nuxeo.com/x/64AIAQ'
    source_link: /display/NXDOC58/How+to+Complete+a+Workflow+Task+Programmatically
history:
    - 
        author: Solen Guitter
        date: '2016-09-01 16:13'
        message: ''
        version: '32'
    - 
        author: Solen Guitter
        date: '2013-11-13 13:46'
        message: ''
        version: '31'
    - 
        author: Solen Guitter
        date: '2013-11-13 13:42'
        message: Updated links to 5.8
        version: '30'
    - 
        author: Mariana Cedica
        date: '2013-10-30 12:11'
        message: ''
        version: '29'
    - 
        author: Solen Guitter
        date: '2013-07-18 14:55'
        message: ''
        version: '28'
    - 
        author: Solen Guitter
        date: '2013-05-16 15:00'
        message: ''
        version: '27'
    - 
        author: Solen Guitter
        date: '2013-04-22 15:08'
        message: ''
        version: '26'
    - 
        author: Mariana Cedica
        date: '2013-04-19 17:57'
        message: ''
        version: '25'
    - 
        author: Mariana Cedica
        date: '2013-04-19 17:49'
        message: ''
        version: '24'
    - 
        author: Mariana Cedica
        date: '2013-04-19 17:46'
        message: ''
        version: '23'
    - 
        author: Mariana Cedica
        date: '2013-04-19 17:46'
        message: ''
        version: '22'
    - 
        author: Mariana Cedica
        date: '2013-04-19 17:45'
        message: ''
        version: '21'
    - 
        author: Mariana Cedica
        date: '2013-04-19 17:44'
        message: ''
        version: '20'
    - 
        author: Mariana Cedica
        date: '2013-04-19 17:41'
        message: ''
        version: '19'
    - 
        author: Mariana Cedica
        date: '2013-04-19 17:39'
        message: ''
        version: '18'
    - 
        author: Mariana Cedica
        date: '2013-04-19 17:38'
        message: ''
        version: '17'
    - 
        author: Mariana Cedica
        date: '2013-04-19 17:37'
        message: ''
        version: '16'
    - 
        author: Mariana Cedica
        date: '2013-04-19 17:28'
        message: ''
        version: '15'
    - 
        author: Mariana Cedica
        date: '2013-04-19 17:25'
        message: ''
        version: '14'
    - 
        author: Mariana Cedica
        date: '2013-04-19 17:24'
        message: ''
        version: '13'
    - 
        author: Mariana Cedica
        date: '2013-04-19 17:20'
        message: ''
        version: '12'
    - 
        author: Mariana Cedica
        date: '2013-04-19 17:19'
        message: ''
        version: '11'
    - 
        author: Mariana Cedica
        date: '2013-04-19 17:16'
        message: ''
        version: '10'
    - 
        author: Mariana Cedica
        date: '2013-04-19 17:13'
        message: ''
        version: '9'
    - 
        author: Mariana Cedica
        date: '2013-04-19 15:26'
        message: ''
        version: '8'
    - 
        author: Mariana Cedica
        date: '2013-04-19 15:22'
        message: ''
        version: '7'
    - 
        author: Mariana Cedica
        date: '2013-04-19 15:11'
        message: ''
        version: '6'
    - 
        author: Mariana Cedica
        date: '2013-04-19 15:00'
        message: ''
        version: '5'
    - 
        author: Mariana Cedica
        date: '2013-04-19 14:56'
        message: ''
        version: '4'
    - 
        author: Mariana Cedica
        date: '2013-04-19 14:55'
        message: ''
        version: '3'
    - 
        author: Mariana Cedica
        date: '2013-04-19 14:53'
        message: ''
        version: '2'
    - 
        author: Mariana Cedica
        date: '2013-04-19 14:37'
        message: ''
        version: '1'

---
{{#> callout type='info' }} {{! excerpt}}

You might need this to implement some sort of automatic processing instead of having the user completing the task from the UI.

{{! /excerpt}} {{/callout}}

Basically, you have to call:

```java
    void endTask(CoreSession session, Task task, Map<String, Object> data,  String status) throws ClientException;
```

on the&nbsp;[DocumentRoutingService](http://community.nuxeo.com/api/nuxeo/5.8/javadoc/org/nuxeo/ecm/platform/routing/api/DocumentRoutingService.html) <span class="componentTitle">, where:</span>

*   <span class="componentTitle">task is the [Task](http://community.nuxeo.com/api/nuxeo/release-5.8/javadoc/org/nuxeo/ecm/platform/task/Task.html) to end;</span>
*   <span class="componentTitle">data is a map of variables. If a variable called "comment" is contained in this map,&nbsp;its value will be logged by the audit service under the "workflowTaskCompleted" event.</span>
    <span class="componentTitle">When a user submits the task form ([configured via Studio]({{page space='studio' page='node-form-tab'}})), this map contains all the variables in the form;</span>
    <span class="componentTitle"><span class="componentTitle">If you want to set an existing Workflow or a Node variable when completing the task you can add them into this map.</span></span>
*   <span class="componentTitle">status is the id of the button the user would have clicked to submit the task form (if the outgoing transitions of the workflow node that created the task</span> have [conditions]({{page space='studio' page='node-form-tab'}}) depending on it).
    This id is the button id you specified when you configured the [task form]({{page space='studio' page='node-form-tab'}}) in Studio.

In your graph, you have nodes and transitions between these nodes. When the workflow enters a node, if that node is of type Task (that means is not an automatic one, like Start and Stop for example), a task is created at that step. This task is persisted as a document model, that can be adapted to the <span class="componentTitle">[Task](http://community.nuxeo.com/api/nuxeo/release-5.8/javadoc/org/nuxeo/ecm/platform/task/Task.html)</span> object. When a task is ended, the workflow is resumed. The task is holding information about the node and the workflow instance it was created from, so when the task is ended using the API above, the related workflow instance is resumed.

To fetch all the open tasks assigned to a given user, on a document use:

```java
  List<Task> getTaskInstances(DocumentModel dm, NuxeoPrincipal user, CoreSession coreSssion) throws ClientException;
```

on the [TaskService](http://community.nuxeo.com/api/nuxeo/5.8/javadoc/org/nuxeo/ecm/platform/task/TaskService.html).

To fetch all the open tasks originating from the same node in the workflow use:

```java
List<Task> getAllTaskInstances(String processId, String nodeId, CoreSession session) throws ClientException;
```

where:

*   processId is the id of the document representing the [workflow instance]({{page page='how-to-modify-a-workflow-variable-outside-of-workflow-context'}}).
*   node id, is a unique identifier of that node in the workflow, generated by Studio. It's listed on the [General tab]({{page space='studio' page='node-general-tab'}}), on the node popup-up when editing a workflow node in Studio.

For some detailed examples on how to use this API, you can check the JUnit tests in the [GraphRouteTest](https://github.com/nuxeo/nuxeo-platform-document-routing/blob/release-5.8/nuxeo-platform-document-routing-core/src/test/java/org/nuxeo/ecm/platform/routing/test/GraphRouteTest.java).

&nbsp;