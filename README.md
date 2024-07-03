# Swift Package Manager for LinkedIn Sign In

- Originally created by [Serhii Londar](https://github.com/serhii-londar/LinkedInSignIn), I just put it into swift package

---

1. Install package: https://github.com/DevboiDesigns/LinkedIn.SignIn-SPM
2. Setup app on [LinkedIn](https://developer.linkedin.com)
3. `import LinkedIn_SignIn`
4. -

```swift
let linkedinCredentilas = [
    "linkedInKey": "",
    "linkedInSecret": "",
    "redirectURL": ""
]
```

5. Login proces

```swift
let linkedInConfig = LinkedInConfig(linkedInKey: linkedinCredentilas["linkedInKey"]!, linkedInSecret: linkedinCredentilas["linkedInSecret"]!, redirectURL: linkedinCredentilas["redirectURL"]!)
let linkedInHelper = LinkedinHelper(linkedInConfig: linkedInConfig)
linkedInHelper.login(from: self, completion: { (accessToken) in
 // DO STUFF
}
```

---

# License

LinkedInSignIn is available under the MIT license. See the LICENSE file for more info.
