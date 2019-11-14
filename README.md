# storyboardless
Setting up a storyboardless project in iOS 11.

1. Delete Storyboard
2. Go to target -> Project -> Delete "Main"
3. Go to Info.plist search for Main, and Delete the entire key value pair.
3. Go to the file SceneDelegate.swift -> and Scene willConnectTo delegate
4. Add the code below inside the delegate.
5. If you like to test it. Go to the ViewController an add a background color in ViewDidLoad.

        guard let windowScene = (scene as? UIWindowScene) else { return }
        window = UIWindow(frame: windowScene.coordinateSpace.bounds)
        window?.windowScene = windowScene
        window?.rootViewController = ViewController()
        window?.makeKeyAndVisible()
