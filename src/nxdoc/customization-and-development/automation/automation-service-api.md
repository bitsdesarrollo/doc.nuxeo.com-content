---
title: Automation Service API
review:
    comment: ''
    date: ''
    status: ok
toc: true
confluence:
    ajs-parent-page-id: '17334309'
    ajs-parent-page-title: Automation
    ajs-space-key: NXDOC58
    ajs-space-name: 'Nuxeo Platform Developer Documentation - 5.8 '
    canonical: Automation+Service+API
    canonical_source: 'https://doc.nuxeo.com/display/NXDOC58/Automation+Service+API'
    page_id: '17334519'
    shortlink: 94AIAQ
    shortlink_source: 'https://doc.nuxeo.com/x/94AIAQ'
    source_link: /display/NXDOC58/Automation+Service+API
history:
    - 
        author: Vladimir Pasquier
        date: '2013-10-23 12:15'
        message: ''
        version: '5'
    - 
        author: Vladimir Pasquier
        date: '2013-10-23 12:09'
        message: ''
        version: '4'
    - 
        author: Vladimir Pasquier
        date: '2013-10-23 12:02'
        message: ''
        version: '3'
    - 
        author: Vladimir Pasquier
        date: '2013-10-23 11:56'
        message: ''
        version: '2'
    - 
        author: Vladimir Pasquier
        date: '2013-10-23 11:29'
        message: ''
        version: '1'

---
<div class="row"><div class="column medium-8">

On server side, [AutomationService](http://community.nuxeo.com/api/nuxeo/5.8/javadoc/org/nuxeo/ecm/automation/AutomationService.html) can be used to:

*   Run contributed chain with chain/operations
*   Run runtime chain created on the fly
*   Run contributed operation

This service provides chain(s)/operation(s) parameters setting and [OperationContext](http://community.nuxeo.com/api/nuxeo/5.8/javadoc/org/nuxeo/ecm/automation/OperationContext.html) instantiation to inject Automation input(s).

</div><div class="column medium-4">{{#> panel heading='In this section'}}

{{/panel}}</div></div>

## Run contributed chain with chain/operations

Chain Contribution:

```
<extension point="chains"
             target="org.nuxeo.ecm.core.operation.OperationServiceComponent">
<chain id="contributedchain">
      <param type="string" name="paramChain" />
      <operation id="o1">
        <param type="string" name="param1">Hello 1!</param>
      </operation>
      <operation id="o2">
        <param type="string" name="param2">Hello 2!</param>
      </operation>
</chain>
</extension>
```

Automation Service API - with chain parameter setting:

```
org.nuxeo.ecm.core.api.DocumentModel doc;
org.nuxeo.ecm.automation.AutomationService service;
org.nuxeo.ecm.core.api.CoreSession session;

// Input setting
org.nuxeo.ecm.automation.OperationContext ctx = new OperationContext(session);
ctx.setInput(doc);
// Setting parameters of the chain
Map<String, Object> params = new HashMap<String, Object>();
params.put("paramChain", "Hello i'm a parameter chain!");
// Run Automation service
service.run(ctx, "contributedchain", params);
```

## Run runtime chain created on the fly

Automation Service API - with chain/operations parameters setting:

```
org.nuxeo.ecm.core.api.DocumentModel doc;
org.nuxeo.ecm.automation.AutomationService service;
org.nuxeo.ecm.core.api.CoreSession session;

// Input setting
org.nuxeo.ecm.automation.OperationContext ctx = new OperationContext(session); 
ctx.setInput(doc);
org.nuxeo.ecm.automation.OperationChain chain = new OperationChain("notRegisteredChain"); 
// Adding operations - operations parameters setting
chain.add("Document.Fetch"); 
chain.add("o1").set("param1", "Hello 1!"); 
chain.add("o2").set("param2", "Hello 2!"); 
// Setting parameters of the chain 
Map<String, Object> params = new HashMap<String, Object>(); 
params.put("messageChain", "Hello i'm a chain!"); 
chain.addChainParameters(params);
// Run Automation service
service.run(ctx, chain);
```

## Run contributed operation

Operation Contribution:

```
  <extension point="operations"
             target="org.nuxeo.ecm.core.operation.OperationServiceComponent">
    <operation class="org.nuxeo.ecm.automation.core.test.Operation1" />
  </extension>
```

Java Class Operation:

```
@Operation(id = "o1")
public class Operation1 {

    @Param(name = "message")
    protected String message;

    @OperationMethod
    public DocumentModel run(DocumentModel doc) throws Exception {
        return doc;
    }

}
```

Automation Service API - with operations parameters setting:

```
org.nuxeo.ecm.core.api.DocumentModel doc;
org.nuxeo.ecm.automation.AutomationService service;
org.nuxeo.ecm.core.api.CoreSession session;

// Input setting
org.nuxeo.ecm.automation.OperationContext ctx = new OperationContext(session); 
ctx.setInput(doc);
// Operation1 parameter setting
Map<String,Object> params = new HashMap<String,Object>(); 
params.put("message","messageValue"); 
service.run(ctx, "o1", params);
```