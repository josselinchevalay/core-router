core-router
===========

Implement SPA arc on polymer platform

Install
==============

```bash

bower install core-router --save
```


Use
=============

Case 1 : Use core-router

for use the component add import on index.html

```html
<link rel="import" href="../components/core-router/core-router.html">
```

declare router : 
```html
<core-router name="Toto" root="Map" pageError="Map" routes='{"Map":"aston-page1","Test":"aston-page2",
     "Error": "aston-page3"}' defaultContainerId="body"></core-router>
```

declare own page (personal polymer component)
```html
<link rel="import" href="../aston/page1.html">
<link rel="import" href="../aston/page2.html">
```

redirect 
```javascript
document.Toto.redirect("Map", null, null);
```

Case 2 : User core-router and core-router-router-hleper-selectable

for use the component add import on index.html

```html
<link rel="import" href="../components/core-router/core-router.html">
<link rel="import" href="../components/core-router/core-router-router-helper-selectable.html">
```

declare router : 
```html
<paper-tabs valueattr="name" selected="Map" self-en>
       <paper-tab name="Map">Map</paper-tab>
       <paper-tab name="Test">Test</paper-tab>
       <paper-tab name="Error">Error</paper-tab>
</paper-tabs>
<core-router name="Toto" root="Map" pageError="Map" routes='{"Map":"aston-page1","Test":"aston-page2",
     "Error": "aston-page3"}' defaultContainerId="body"></core-router>
<core-router-router-helper-selectable selectableElementId="paper-tabs" routerName="Toto"></core-router-router-helper-selectable>
```

declare own page (personal polymer component)
```html
<link rel="import" href="../aston/page1.html">
<link rel="import" href="../aston/page2.html">
```

the redirection is automatic ! 



