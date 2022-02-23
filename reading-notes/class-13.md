# Local Storage

- Web applications need a way to store persistent information that is not sent to the server. Since this information is stored client side, a lot of storage space is required.
- Cookies allow for limited storage of user information, but are slow and unencrypted
- Some of these problems have been solved in html5 usin web storage
- Web storage is a way for pages to stor key/value pairs locally
- Web storage data persists after users navigate away from the web site, and is not transmitted to the server
- Web storage data is stored and retrieved using the same named key. This can be any data type supported by JavaScript
- Local Storage can be treated as an array in JS, accessed using square brackets
- Changes to the storage can be monitored using an event listener in JS
- A limitation of this html5 storage space is its 5mb size limitation
- This technology is still being iterated, and there are many competeing visions for future implementation
