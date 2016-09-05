---
title: Actions Display
labels:
    - action
toc: true
confluence:
    ajs-parent-page-id: '17334390'
    ajs-parent-page-title: 'Actions (Links, Buttons, Icons, Tabs and More)'
    ajs-space-key: NXDOC58
    ajs-space-name: 'Nuxeo Platform Developer Documentation - 5.8 '
    canonical: Actions+Display
    canonical_source: 'https://doc.nuxeo.com/display/NXDOC58/Actions+Display'
    page_id: '18449688'
    shortlink: GIUZAQ
    shortlink_source: 'https://doc.nuxeo.com/x/GIUZAQ'
    source_link: /display/NXDOC58/Actions+Display
history:
    - 
        author: Solen Guitter
        date: '2016-09-01 08:51'
        message: ''
        version: '4'
    - 
        author: Solen Guitter
        date: '2014-03-11 12:03'
        message: ''
        version: '3'
    - 
        author: Solen Guitter
        date: '2014-01-23 18:11'
        message: ''
        version: '2'
    - 
        author: Solen Guitter
        date: '2014-01-22 17:30'
        message: ''
        version: '1'

---
<div class="row"><div class="column medium-8">{{! excerpt}}

Actions are grouped in categories to be able to display them in the same area of a page. Widgets can be used to handle rendering of these actions.

{{! /excerpt}}

Actions are referencing the same category when they need to be displayed in the same area of a page.

The available categories are listed below and can also be found by checking action contributions on [the explorer](http://explorer.nuxeo.org/nuxeo/site/distribution/Nuxeo%20Platform-5.8/viewExtensionPoint/org.nuxeo.ecm.platform.actions.ActionService--actions).

## CAP Categories

{{{multiexcerpt 'CAP-actions-categories-1' page='Studio:User actions categories'}}}

</div><div class="column medium-4">{{#> panel heading='In this section'}}

{{/panel}}</div></div>

{{{multiexcerpt 'CAP-actions-categories-2' page='Studio:User actions categories'}}}

## CAP Advanced Categories

These categories can be useful when defining custom actions, that will reference the widgets to display. This is useful when building incremental layouts, like the default summary layout starting from 5.6: the action order and filter information are useful to contribute/display/hide some widgets to the summary default layout.

These categories are not really useful when defining user actions, and the associated features can be broken when migrating from 5.6 to 5.8, as the form around the summary layout has been removed for 5.8 to allow fine-grained form management on this page.

### View Action List

Technical name: `VIEW_ACTION_LIST`.

This categories is used for tabs displayed on every document.

```html/xml
<action id="TAB_VIEW" link="/incl/tabs/document_view.xhtml" enabled="true"
  order="0" label="action.view.summary" type="rest_document_link">
  <category>VIEW_ACTION_LIST</category>
  <filter-id>view</filter-id>
</action>

<action id="TAB_CONTENT" link="/incl/tabs/document_content.xhtml" order="10"
  enabled="true" label="action.view.content" type="rest_document_link">
  <category>VIEW_ACTION_LIST</category>
  <filter-id>view_content</filter-id>
</action>

```

{{{multiexcerpt 'CAP-advanced-actions-categories' page='Studio:User actions categories'}}}

## DAM Categories

{{{multiexcerpt 'DAM-actions-categories' page='Studio:User actions categories'}}}

## {{> anchor 'adapt-templates-to-display-action'}}Adapting Templates to Display an Action

Since Nuxeo Platform 5.6, an action can define the way it will be rendered by using the&nbsp;`type` attribute. This make it easier to combine different kinds of rendering for a group of actions, and this is done by using widget types for action types, to leverage features from the [Nuxeo Layout Framework]({{page page='layouts-and-widgets-forms-listings-grids'}}).

The [ `template` action type]({{page page='standard-action-types'}}) makes it possible to define a custom action rendering. [New action types]({{page page='custom-action-types'}}) can also be contributed to the framework.

A series of widget types displaying are available by default, see the pages [Tab Designer Widget Types]({{page page='tab-designer-widget-types'}}) and [Advanced Widget Types]({{page page='advanced-widget-types'}}). These widget types include rendering configuration options that are implemented by default action widget types (CSS styling, display as buttons or links, for instance).

Here are two ways of rendering actions.

### Rendering Actions via Widget Definitions

Here is a sample widget definition to render actions using category `MY_CATEGORY`:

```xml
<extension target="org.nuxeo.ecm.platform.forms.layout.WebLayoutManager"
  point="widgets">
  <widget name="userActions" type="documentActionsWithForms">
    <properties mode="view">
      <property name="category">MY_CATEGORY</property>
      <property name="actionsDisplay">links</property>
      <property name="overallDisplay">horizontal_block</property>
      <property name="styleClass">userActions</property>
    </properties>
  </widget>
</extension>
```

This widget can be displayed on a page directly using the following sample code:

```xml

<div xmlns:nxl="http://nuxeo.org/nxforms/layout">
  <nxl:widget name="userActions" mode="view" value="#{currentDocument}" />
</div>
```

Of course this widget definition can also be included within a layout definition, as it's done for [Incremental Layouts]({{page page='incremental-layouts-and-actions'}}) configuration.

### Rendering Actions via Dynamically Computed Widget

It can also be useful to generate the widget definition dynamically from the widget template, by passing the widget properties as tag attributes to the&nbsp;`nxl:widgetType` tag:

```xml

<div xmlns:nxl="http://nuxeo.org/nxforms/layout">
  <nxl:widgetType name="documentActionsWithForms"
    widgetName="documentActionsUpperButtons"
    mode="view"
    label=""
    actionStyleClass="button"
    actionsDisplay="icons"
    overallDisplay="horizontal_block"
    widgetProperty_category="MY_CATEGORY"
    maxActionsNumber="5"
    value="#{currentDocument}" />
</div>
```

Notice the tag attribute `widgetProperty_category` used to define the actions category: as widget types also have a notion of category, adding&nbsp;`widgetProperty_` prefix to the attribute makes it possible to explicitly state that this is a widget property.

See also chapter about [Layout and Widget Display]({{page page='layout-and-widget-display'}}).

* * *

<div class="row" data-equalizer data-equalize-on="medium"><div class="column medium-6">{{#> panel heading='Related sections in this documentation'}}

*   [Actions Overview]({{page page='actions-overview'}})
*   [Standard Action Types]({{page page='standard-action-types'}})
*   [Custom Action Types]({{page page='custom-action-types'}})

{{/panel}}</div><div class="column medium-6">{{#> panel heading='Related sections in Studio documentation'}}

*   [User Actions]({{page space='studio' page='user-actions'}})

{{/panel}}</div></div>