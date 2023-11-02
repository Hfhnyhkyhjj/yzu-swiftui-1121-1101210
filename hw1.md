<h1>HW1</h1>
    
```swift

      import SwiftUI

struct ContentView: View{
    var body: some View{
         Image(systemName: "cloud")
            .font(.system(size:50))
            .foregroundColor(.gray)
            .frame(width:350,height:0,alignment:.leading)
        Image(systemName: "cloud")
            .font(.system(size:70))
            .foregroundColor(.secondary)
            .frame(width:250,height:25,alignment:.leading)
        Image("A")
            .resizable()
            .aspectRatio(contentMode: .fit)
            .overlay(
               
                     Text("s1101210 余頻青\r\nBetter late than never.")
                     
                    .fontWeight(.heavy)
                    . lineSpacing(20)
                    .font(.system(size:32.0))
                    .foregroundColor(.white)
                    .frame(width:350,height:150,alignment:.center)
                    .background(Color.secondary)
                    .cornerRadius(30.0)
                    .opacity(0.8)
                ,
                alignment: .bottom
            )
    }
}





    
```

<img width="40%"  src="https://raw.githubusercontent.com/ncudemo/yzu-swiftui-1121-1101210/main/IMG_0350.png">
