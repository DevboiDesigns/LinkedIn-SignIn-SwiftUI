# Swift Package Manager for LinkedIn Sign In

- Originally created by [Serhii Londar](https://github.com/serhii-londar/LinkedInSignIn), I just put it into swift package

---

1. Install package: https://github.com/DevboiDesigns/LinkedIn.SignIn-SPM
2. Setup app on [LinkedIn](https://developer.linkedin.com)
3. `import LinkedIn_SignIn`
4. Credentials Helper

```swift
let linkedinCredentilas = [
    "linkedInKey": "",
    "linkedInSecret": "",
    "redirectURL": ""
]
```

5. Login proces - Opens a web view to sign and get access token, token can be used via the LinkedIn SignIn [API](https://developer.linkedin.com)

```swift
let linkedInConfig = LinkedInConfig(linkedInKey: linkedinCredentilas["linkedInKey"]!, linkedInSecret: linkedinCredentilas["linkedInSecret"]!, redirectURL: linkedinCredentilas["redirectURL"]!)
let linkedInHelper = LinkedinHelper(linkedInConfig: linkedInConfig)
linkedInHelper.login(from: getRootViewController(), completion: { (accessToken) in
 // DO STUFF
}
```

GET ROOT VIEW CONTROLLER

```swift
 static public func getRootViewController() -> UIViewController {
        guard let screen = UIApplication.shared.connectedScenes.first as? UIWindowScene else { return .init() }
        guard let root = screen.windows.first?.rootViewController else { return .init() }
        return root
    }
```

---

# License

LinkedInSignIn is available under the MIT license. See the LICENSE file for more info.
