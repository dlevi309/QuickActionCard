# QuickActionCard

Displays a customizable quick action card. <br>
Please feel free to use this file in any of your projects!
<br>
<br>
<img src="https://github.com/Leon12345679/QuickActionCard/blob/master/screenshots/IMG_0319.PNG" width="300" alt="preview"/>

# Usage Example
```swift
struct ContentView: View {
    @State private var quickActionShown: Bool = false

    var body: some View {
        ZStack {
            Button("Show Card") {
                withAnimation {
                     self.quickActionShown.toggle()
                }
            }

            if quickActionShown {
                CardView(isPresented: $quickActionShown) {
//                  Your view to display in the card
                    VStack {
                        Text("Hello World!")
                            .font(.largeTitle)
                        HStack {
                            Text("Feel Free to use this. ")
                            Text("Anywhere...")
                        }

                        Text("🧐")
                            .font(.largeTitle)
                    }
                }

//              Modifiers
                .enableHapticFeedback()
                .dismissButton()
            }
        }
    }
}
```

# Current Modifiers
<ul>
<li>overlayParent</li>
<li>enableHapticFeedback</li>
<li>tapToDismiss</li>
<li>dismissButton</li>
<li>cardCornerRadius</li>
</ul>

# Default Behavior 
The card appears with a slide in from bottom transition. <br>
The parent overlay appears with an opacity transition (if you use the overlayParent modifier). <br>

# Contact Info
You can reach me here: <br>
Leon.Vladimirov@gmail.com
