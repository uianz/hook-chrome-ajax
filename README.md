

A chrome extension for modifing response text of ajax requests easily. You can use it to debug errors.


## Notes
1. You may have to restart chrome or refresh the current page after you added this extension.
2. It is recommended that you turn off this extension(the icon should be gray) when you are not using it.
3. This extension only overrides the response data in the XMLHTTPRequest object as well as the fetch method. The "real" response which you can see in DevTools' "Network" panel will not be changed.

code reference https://raw.githubusercontent.com/YGYOOO/ajax-interceptor/master/

manifest v2 upgrade v3 api:
```
chrome.extension.sendRequest() => chrome.runtime.sendMessage()
chrome.extension.onRequest => chrome.runtime.onMessage
chrome.extension.onRequestExternal => chrome.runtime.onMessageExternal
chrome.extension.lastError => chrome.runtime.lastError
chrome.extension.getURL() => chrome.runtime.getURL()
chrome.extension.getExtensionTabs() => chrome.extension.getViews()
chrome.tabs.Tab.selected => chrome.tabs.query({active: true})
chrome.tabs.sendRequest() => chrome.runtime.runtime.sendMessage()
chrome.tabs.getSelected() => chrome.tabs.query({active: true})
chrome.tabs.getAllInWindow() => chrome.tabs.query({currentWindow: true})
chrome.tabs.onSelectionChanged => chrome.tabs.onActivated()
chrome.tabs.onActiveChanged => chrome.tabs.onActivated()
chrome.tabs.onHighlightChanged => chrome.tabs.onHighlighted

chrome.extension.sendMessage() => chrome.runtime.sendMessage()
chrome.extension.connect() => chrome.runtime.connect()
chrome.extension.onConnect => chrome.runtime.onConnect
chrome.extension.onMessage => chrome.runtime.onMessage
```