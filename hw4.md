<h1>HW4</h1>
    
```swift

//MyApp

import SwiftUI

@main
struct MyApp: App {
    var body: some Scene {
        WindowGroup {
            ContentView()
        }
    }
}
//-------------------------separate line-------------------------

//ContentView

import SwiftUI

struct ContentView: View{
    var body:some View{
        VStack{
        Text("2023 10月 動漫新番推薦")
                .font(.title)
            .fontWeight(.heavy)
            .foregroundStyle(.primary)
        TabView{
            Group{
            WelcomeView()
                .tabItem{
                    Image(systemName: "rosette")
                    Text("Welcome")
                }
            CourseListView()
                .tabItem{
                    Image(systemName: "list.dash")
                    Text("List")
                }
            CardView()
                .tabItem{
                    Image(systemName: "book")
                    Text("TOP")
                }
        }
            .toolbarBackground(Color.black,for:.tabBar)
            .toolbarBackground(.visible,for:.tabBar)
        }
        .tint(.yellow)
    }
    }
}
//-------------------------separate line-------------------------

//WeicomeView

import SwiftUI
struct WelcomeView: View{
var body: some View { 
    VStack{
    Image("image")
        .resizable().aspectRatio(contentMode: .fit)
    Text("劇情簡介/開播資訊")
        .fontWeight(.heavy)
        .lineSpacing(20)
        .font(.system(size: 32.0))
        .foregroundColor(.white)
        .frame(width: 350, height: 150, alignment: .center)
        .background(Color.red)
        .cornerRadius(20.0)
        .multilineTextAlignment(.center)
}}}
//-------------------------separate line-------------------------

//CourseListView

import SwiftUI

struct Course:Identifiable{
    var id = UUID()
    var name:String
    var image:String
    var description:String
}
var courses = [
    Course(name: "葬送的芙莉蓮", image: "1", description: "故事大綱：\n身為精靈族的芙莉蓮與同伴欣梅爾、艾冉、海塔花了10年打倒了魔王凱旋回到王都，眾人接受了國王接見與表揚。正值每隔50年出現一次的半世紀流星雨，芙莉蓮還天真地說下次要帶大家去一個很棒的地方欣賞流星。然而50年對於身為精靈的她根本不算什麼，然而下次見面時欣梅爾已經成了老頭子，還自嘲這是最後一次跟大家相聚。後來欣梅爾的離世讓芙莉蓮開始思考時間與生命的意義…。\n\n播放日：2023年10月6日起／每週五／23時0分"),
    Course(name: "SPY×FAMILY 間諜家家酒 Season 2", image: "2", description: "故事大綱：\n約兒接下東國（Ostania）祕密組織「花園」的任務，將登上豪華郵輪，護衛黑手黨要人！\n然而洛伊德和安妮亞也將搭乘同一艘船去旅遊，這讓約兒對自己的祕密工作萌生迷惘？\n\n播放日：2023年10月7日起／每週六／23時0分"),
    Course(name: "我想成為影之強者！2nd season", image: "3", description: "故事大綱：\n在克萊兒提議之下，席德來到「無法治都市」。在那裡，他參加了討伐沉眠的吸血鬼始祖「噬血女王」的任務。而後，出現在他眼前的，是自稱「最資深的吸血鬼獵人」的神祕美少女瑪莉。\n除了「無法治都市」的三大勢力「暴君」加格諾、「妖狐」雪女、「吸血鬼」克里姆森以外，「闇影庭園」也為了尋求「始祖血脈」和「惡魔附體者」的關連而參戰，讓戰場變得一片混亂。\n同時，「傳說的始祖」覺醒的時刻也跟著逼近……！\n\n播放日：2023年10月4日起／每週三／22時30分"),
    Course(name: "香格里拉·開拓異境", image: "4", description: "故事大綱：\n你是為了什麼而玩遊戲的？如果世上有100部神作，那麼也存在著1000部糞作。這是喜愛糞作，同時也被糞作所愛的男人“陽務樂郞”，向糞作的反面——神作「香格里拉·開拓異境」發起挑戰的故事。\n陽務樂郎是一個超愛玩“糞作”的糞作玩家，玩家名稱名為桑樂，擁有超一流的電玩技術！某天一個小小的契機讓他開始挑戰大眾公認的神作電玩。沒但想到電玩世界和現實生活卻都因此開始以他為中心產生變化…\n\n播放日：2023年10月1日起／每週日／17時0分"),
    Course(name: "藥師少女的獨語", image: "5", description: "故事大綱：\n「可否為我配製一帖春藥？」 貓貓的眼眸瞬間浮現出驚訝與好奇的色彩－－\n位處大陸中央的某個大國，有位姑娘置身於皇帝宮闕之中。 姑娘名喚貓貓，原在煙花巷擔任藥師，眼下則在後宮做下女。\n 這個絕對稱不上美女的姑娘很懂分寸，只是靜待期滿離宮。 她有自信，皇帝絕對不會「寵幸」她。 \n其間，貓貓得知皇子皆年幼早夭的事， 並聽聞連尚在人世的皇子皇女也身染重病，她開始調查他們的病因－－\n\n播放時間：2023年10月28日起／每週六深夜／24時55分"),
    Course(name: "不死不運", image: "6", description: "故事大綱：\n某天，出雲風子（不運）再也受不了自己總是給身旁的人帶來不幸，決定一死了之；此時卻突然出現一名全身赤裸的神秘男子（不死），也打算靠她的不幸能力自我了斷。\n然而這個舉動卻讓雙方都無法順利死去，於是決定換地方再死一次，不過這次卻出現某個組織（UNION）派來的追兵，試圖將他們帶回組織。\n不死為了完成心願，帶著不運展開逃亡，他們的命運將會如何？那個組織又是什麼來頭？\n\n播放日：2023年10月6日起／每週五深夜／25時23分"),
    Course(name: "米奇與達利 惡童物語", image: "7", description: "故事大綱：\n1990年神戶市北區。\n有個以美國郊區為原型打造出來的新城──奧里岡村，在這座富裕居民們生活的鎮上出現了「一個人」，他是名少年。\n那個少年是沒有子嗣的園山家收養的孩子，名為秘鳥。\n園山夫妻很快就受到俊美聰穎的少年秘鳥所吸引，但是秘鳥卻有一個天大的祕密與驚人的目的──\n\n播放日：2023年10月2日起／每週一／22時0分"),
    Course(name: "咒術廻戰 第2期", image: "8", description: "故事大綱：\n虎杖他們擊敗道成肉身的「咒胎九相圖」次男和三男，回收了宿儺的手指。\n這個成果令他們獲薦成為１級術師。\n而在背後暗中安排的五條，究竟有何用心…!?\n──故事將追溯到五條和夏油高專２年級時的事件!!\n\n跨季繼續播放：每週四／23時56分")
]

struct BasicImageRow: View{
    var thisCourse:Course
    var body: some View{
        HStack{
            Image(thisCourse.image)
                .resizable()
                .frame(width: 60, height: 70)
                .cornerRadius(5)
            Text(thisCourse.name)
        }
    }
}
struct CourseDetailView:View{
    @Environment(\.presentationMode) var presentationMode
    var thisCourse:Course
    var body: some View{
        ScrollView{
            VStack{
                Image(thisCourse.image)
                    .resizable()
                    .aspectRatio(contentMode: .fill)
                    .clipped()
                Text(thisCourse.name)
                    .font(.system(.title, design:.rounded))
                    .fontWeight(.black)
                Spacer()
                Text(thisCourse.description)
                    .font(.system(.subheadline, design:.rounded))
                    .fontWeight(.light)
                Spacer()
            }
        }
        .overlay(
            HStack{
                Spacer()
                VStack{
                    Button(action:{
                        self.presentationMode.wrappedValue.dismiss()
                    },label:{
                        Image(systemName:"chevron.down.circle.fill").font(.largeTitle)
                            .foregroundColor(.gray)
                    })
                    .padding(.trailing, 20)
                    .padding(.top, 40)
                    Spacer()
                }
            }
        )
    }
}

struct CourseListView:View{
    @State var showDetailView = false
    @State var selectedCourse:Course?
    var body: some View{
        NavigationView{
            List(courses){ courseItem in
                BasicImageRow(thisCourse: courseItem)
                    .onTapGesture{
                        self.showDetailView = true
                        self.selectedCourse = courseItem
                    }
            }
            .sheet(item: self.$selectedCourse){ thisCourse in CourseDetailView(thisCourse: thisCourse)
            }
            .navigationBarTitle("個人推薦新番列表")
        }
    }    
    
}
//-------------------------separate line-------------------------

//CardView

import SwiftUI
struct TermAndDescription: Identifiable{
    var id = UUID()
    var term:String 
    var image:String
    var description:String
}

var myDictionary = [
    TermAndDescription(term: "TOP1\n<葬送的芙莉蓮>",image: "11", description: "網站投票率：12.56%"),
    TermAndDescription(term: "TOP2\n<我想成為影之強者>", image: "22", description: "網站投票率：11.32%"),
    TermAndDescription(term: "TOP3\n<咒術廻戰>", image:"33", description: "網站投票率：7.23%"),
]

struct CardView: View{
    @State var currentCard = 0
    var body: some View{
        VStack{Text("週人氣TOP3")
                .padding(.all, 10)
             .font(.title)
            VStack{
                Image(myDictionary[currentCard].image)
                    .resizable()
                    .frame(width: 200, height: 240)
                    .cornerRadius(5)
                Text(myDictionary[currentCard].term)
                    .font(.title)
                    .foregroundColor(.white)
                    .padding(.all, 10)
                Text(myDictionary[currentCard].description)
                    .font(.body)
                    .foregroundColor(.blue)
                    .padding(.all, 10)
            }
            .frame(minWidth: 0, idealWidth: 100, maxWidth: 300, minHeight: 0, idealHeight: 100, maxHeight: 400, alignment: .center)
            .background(Color.black).onTapGesture{
                if currentCard<myDictionary.count-1{
                    currentCard+=1
                }else{
                    currentCard=0
                }
            }
            Text("點擊查看下一張")
                .padding(.all, 10)
        }
    }
}


```

<img width="40%"  src="https://github.com/Hfhnyhkyhjj/yzu-swiftui-1121-1101210/blob/main/IMG_0352.png">
