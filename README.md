# cordova-ios-s3-security
Cordova plugin to exclude S3 from App Transport Security (iOS9)


# cordova-ios-security
`cordova plugin add https://github.com/pincombe/cordova-ios-s3-security.git`

It will add the following part to the `*-Info.plist` file during build process:

    <dict>
      <key>NSExceptionDomains</key>
      <dict>
        <key>s3.amazonaws.com</key>
        <dict>
          <key>NSIncludesSubdomains</key>
          <true/>
          <key>NSExceptionRequiresForwardSecrecy</key>
          <false/>
        </dict>
      </dict>
    </dict>    
