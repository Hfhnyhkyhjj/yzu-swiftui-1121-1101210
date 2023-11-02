<h1>HW1</h1>
    
```swift

      import SwiftUI
struct ContentView: View{
    var body: some View{
        VStack{
            TitleView()
            HStack{
                 HView(imageName:"H")
              BView(imageName:"B")
            }
            HStack{
                 AView(imageName:"A")
             EView(imageName:"E")
                 FView(imageName:"F")
                 GView(imageName:"G")
                 }
            HStack{ZStack{
                CView(imageName: "C")
                Text("$75")
                    .font(.system(size: 20))
                    .foregroundColor(.white)
                    .padding (.all,5)
                    .background (Color.blue)
                    .opacity(0.7)
                .offset(x: 40, y: 20)}
                ZStack{ DView(imageName: "D")
                Text("$60")
                    .font(.system(size: 20))
                    .foregroundColor(.white)
                    .padding (.all,5)
                    .background (Color.blue)
                    .opacity(0.7)
                .offset(x: 40, y: 20)}
                ZStack{
                    IView(imageName:"I")
                    Text("$70")
                        .font(.system(size: 20))
                        .foregroundColor(.white)
                        .padding (.all,5)
                        .background (Color.blue)
                        .opacity(0.7)
                        .offset(x: 40, y: 20)
                }
            }}
    }
    }
    
    struct TitleView: View {
        var body: some View {
            VStack(alignment:.center,spacing:2){
                Text("Ｙu的")
                    .font(.system(size:30))
                Text("甜點櫃")
                    .font(.title)
                    .foregroundColor(Color(red:29/255,green:40/255,blue:192/255))
            }
        }
    }
    
    struct HView: View {
        var imageName:String
        var body: some View {
            VStack{
                Image ("H")
                    .resizable ()
                    .aspectRatio (contentMode: .fit)
                    .frame (width: UIScreen.screenWidth/2-20, alignment: .center)
                Text ("焦糖布丁")
                    .fontWeight(.bold)
                    .font (.system(size: 20))
            }.padding(.all,2)
        }}
    struct BView: View {
        var imageName:String
        var body: some View {
            VStack{
                Image ("B")
                    .resizable ()
                    .aspectRatio (contentMode: .fit)
                    .frame (width: UIScreen.screenWidth/2-20, alignment: .center)
                Text ("水果布丁")
                    .fontWeight(.bold)
                    .font (.system(size: 20))
            }.padding(.all,2)
        }}
struct AView: View {
    var imageName:String
    var body: some View {
        VStack{
            Image ("A")
                .resizable ()
                .aspectRatio (contentMode: .fit)
                .frame (width: UIScreen.screenWidth/4-30, alignment: .center)
            Text("乳酪蛋糕")
                .fontWeight(.bold)
            .font (.system(size: 20))}
        .padding(.all,2)
    }}
struct CView: View {
    var imageName:String
    var body: some View {
        VStack{
            Image ("C")
                .resizable ()
                .aspectRatio (contentMode: .fit)
                .frame (width: UIScreen.screenWidth/3-30, alignment: .center)
            Text ("檸檬塔")
                .fontWeight(.bold)
                .font (.system(size: 20))
        }.padding(.all,2)
    }}
struct DView: View {
    var imageName:String
    var body: some View {
        VStack{
            Image ("D")
                .resizable ()
                .aspectRatio (contentMode: .fit)
                .frame (width: UIScreen.screenWidth/3-30, alignment: .center)
            Text ("蘋果派")
                .fontWeight(.bold)
                .font (.system(size: 20))
        }.padding(.all,2)
    }}
struct EView: View {
    var imageName:String
    var body: some View {
        VStack{
            Image ("E")
                .resizable ()
                .aspectRatio (contentMode: .fit)
                .frame (width: UIScreen.screenWidth/4-30, alignment: .center)
            Text ("千層蛋糕")
                .fontWeight(.bold)
                .font (.system(size: 20))
        }.padding(.all,2)
    }}
struct FView: View {
    var imageName:String
    var body: some View {
        VStack{
            Image ("F")
                .resizable ()
                .aspectRatio (contentMode: .fit)
                .frame (width: UIScreen.screenWidth/4-30, alignment: .center)
            Text ("波士頓派")
                .fontWeight(.bold)
                .font (.system(size: 20))
        }.padding(.all,2)
    }}
struct GView: View {
    var imageName:String
    var body: some View {
        VStack{
            Image ("G")
                .resizable ()
                .aspectRatio (contentMode: .fit)
                .frame (width: UIScreen.screenWidth/4-30, alignment: .center)
            Text ("提拉米蘇")
                .fontWeight(.bold)
                .font (.system(size: 20))
        }.padding(.all,2)
    }}
struct IView: View {
    var imageName:String
    var body: some View {
        VStack{
            Image ("I")
                .resizable ()
                .aspectRatio (contentMode: .fit)
                .frame (width: UIScreen.screenWidth/3-20, alignment: .center)
            Text ("肉桂捲")
                .fontWeight(.bold)
                .font (.system(size: 20))
        }.padding(.all,2)
    }}
extension UIScreen{ static let screenWidth=UIScreen.main.bounds.size.width
    static let screenHeight=UIScreen.main.bounds.size.height
    static let screenSize=UIScreen.main.bounds.size
}






    
```

<img width="40%"  src="https://github.com/Hfhnyhkyhjj/yzu-swiftui-1121-1101210/blob/main/IMG_0352.png">




