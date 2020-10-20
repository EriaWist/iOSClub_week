//
//  ForView.swift
//  week3
//
//  Created by 阿騰 on 2020/10/19.
//

import SwiftUI

struct ForView: View {
    @State var text:[Text]=[]
    @State var num = [Int]()
    var body: some View {
        VStack {
            VStack{
                ForEach(0..<text.count,id: \.self)
                //\.self 我猜是自身的keypath
                { item in
                    self.text[item]
                    
                }
            }
            
            Button(action: {
                    var r = Int.random(in: 1...100)
                    while num.contains(r) {
                        r = Int.random(in: 1...100)
                    }
                    self.num.append(r)
                    if r>50{
                        text.append(Text("\(r)")
                                        .foregroundColor(Color.red))
                    }
                    else
                    {
                        text.append(Text("\(r)"))
                    }
                
                
                
            }) {
                Text("add")
            }
        }
    }
}

struct ForView_Previews: PreviewProvider {
    static var previews: some View {
        Group {
            ForView()
        }
    }
}
