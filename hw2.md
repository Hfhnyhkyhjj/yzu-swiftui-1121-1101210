<h1>HW2</h1>
    
```swift

      import SwiftUI

struct ContentView: View {
    @State var a:String="🤡"
    @State var b:String="開始"
    var body: some View {
        VStack{
            Text(String(b))
                .frame(width:150,height:100)
            .font(.system(size:30))
            Text(String(a))
                .padding(.all,10)
                .frame(width:150,height:120,alignment:.center)
            .font(.system(size:100))}
        HStack{
            Button(action:{
                let randomIV=Int.random(in:0...2)
                if randomIV==0{
                  b="平手"
                    a="✌️"}
                else if randomIV==1{b="你輸了"
                    a="👊"}
                else{b="你贏了"
                    a="✋"}
                
            },label:{
                Text("✌️")
                    .padding(.all,10)
                    .frame(width:70,height:70,alignment:.center)
                    .font(.system(size:50))
                    .background(Color.purple)
                    .foregroundColor(.white)
                    .border(Color.purple,width:5)
                    .cornerRadius(20)
            })
            Button(action:{
                let randomIV=Int.random(in:0...2)
                if randomIV==0{
                    b="你贏了"
                    a="✌️"}
                else if randomIV==1{
                    b="平手"
                    a="👊"}
                else{
                    b="你輸了"
                    a="✋"}
                
            },label:{
                Text("👊")
                    .padding(.all,10)
                    .frame(width:70,height:70)
                    .font(.system(size:50))
                    .background(Color.purple)
                    .cornerRadius(20)
            })
            Button(action:{
                let randomIV=Int.random(in:0...2)
                if randomIV==0{
                    b="你輸了"
                    a="✌️"}
                else if randomIV==1{
                    b="你贏了"
                    a="👊"}
                else{
                    b="平手"
                    a="✋"}
                
            },label:{
                Text("✋")
                    .padding(.all,10)
                    .frame(width:70,height:70)
                    .font(.system(size:50))
                    .background(Color.purple)
                    .cornerRadius(20)
            })
        }
    }
}






    
```
<iframe style="width:560px; height:315px;" src="https://github.com/Hfhnyhkyhjj/yzu-swiftui-1121-1101210/blob/main/RPReplay_Final1698895309.mp4" frameborder="0" allowfullscreen></iframe>
