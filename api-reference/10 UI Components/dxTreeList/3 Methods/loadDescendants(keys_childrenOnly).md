---
id: dxTreeList.loadDescendants(keys, childrenOnly)
---
---
##### shortDescription
Loads all or only direct descendants of specific nodes. Takes effect only if data has the [plain structure](/api-reference/10%20UI%20Components/dxTreeList/1%20Configuration/dataStructure.md '/Documentation/ApiReference/UI_Components/dxTreeList/Configuration/#dataStructure') and  **remoteOperations**.[filtering](/api-reference/10%20UI%20Components/dxTreeList/1%20Configuration/remoteOperations/filtering.md '/Documentation/ApiReference/UI_Components/dxTreeList/Configuration/remoteOperations/#filtering') is **true**.

##### return: Promise<void>
A Promise that is resolved after data is loaded. It is a <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise" target="_blank">native Promise</a> or a <a href="http://api.jquery.com/Types/#Promise" target="_blank">jQuery.Promise</a> when you use jQuery.

##### param(keys): Array<any>
Node keys.

##### param(childrenOnly): Boolean
Pass **true** to load only children, **false** to load all the specified node's descendants.          
**false** by default.

---
