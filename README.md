# iOS-awesome-tips

## Keyboard
Fixing the keyboard: NotificationCenter
- https://www.hackingwithswift.com/read/19/7/fixing-the-keyboard-notificationcenter

But, most solutions tend to be quite DIY, and have to be implemented for each view controller that needs it.
https://github.com/michaeltyson/TPKeyboardAvoiding

## UILabel
Make part of a UILabel bold in Swift
- https://stackoverflow.com/questions/36486761/make-part-of-a-uilabel-bold-in-swift

```swift
private func attributedText(withString string: String, targetString: String, color: UIColor) -> NSAttributedString {
    let normalAttributes = [NSAttributedString.Key.foregroundColor: UIColor.gray700,
                            NSAttributedString.Key.font: UIFont.notoSansMediumFontOfSize(size: 12)]
    let attributedString = NSMutableAttributedString(string: string, attributes: normalAttributes)
    let targetColorAttribute: [NSAttributedString.Key: Any] = [NSAttributedString.Key.foregroundColor: UIColor.ceruleanBlue]
    let range = (string as NSString).range(of: targetString)
    attributedString.addAttributes(targetColorAttribute, range: range)
    return attributedString
}
```
