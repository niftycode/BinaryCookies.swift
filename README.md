# BinaryCookies.swift

Cookie parser for Safari's `Cookies.binarycookies` files, located in

	~/Library/Cookies

This is the Swift3 version of the "BinaryCookies.swift", forked from [icodeforlove](https://github.com/icodeforlove/BinaryCookies.swift).

# Cookie Data

each cookie contains the following data

- expiration
- creation
- domain
- name
- path
- value
- secure
- http

# Usage

```swift
BinaryCookies.parse(NSHomeDirectory() + "/Library/Cookies/Cookies.binarycookies", callback: {
    (error:BinaryCookiesError?, cookies) in

    if let cookies = cookies {
        print(cookies);
    } else {
        print(error);
    }
});
```