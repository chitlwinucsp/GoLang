ကျွန်တော်ကတော့  IDE (Integrated development editor) ကို vs code ကိုသုံးပါတယ်။

အရင်ဆုံးက go ကို official side ကနေသွားပြီး ကိုယ့်ရဲ့ os ပေါ် မူတည်ပြီး [download](https://go.dev/dl/) ချပါ။

vs code ကနေ  go extension [ဒီလင့်ကနေ](https://marketplace.visualstudio.com/items?itemName=golang.Go) သွင်းပါမယ်။
vs code extension browser မှာလဲ ရှာပြီးသွင်းလို့ရပါတယ်။ 

အရင်ဆုံး ကိုယ့်ရဲ့ စက်မှာ path လမ်းကြောင်း မှန်မှန်ကန်ကန်ဖြစ်ပြီး အဆင်ပြေပြေဖြစ်လားဆိုတာကို vs code terminal ကနေ ဒီလိုမျိုး ရိုက်ပြီး စတင်ကြည့်ပါ။

```
➜  go version
```

**go version gox.xxx windows/amd64** ပေါ်ရင် အဆင်ပြေပါတယ်။

နောက်တစ်ခုက  helloword.go ကို အောက်ပါအတိုင်းဆောက်ပါ

```
package main

import "fmt"

func main() {
	fmt.Println("Hello, World!")
}

```

အဲ့လိုဆောက်ပြီးပေမဲ့ ကိုယ်က run ချင်နေပြီဆိုပါတော့ ဘယ်လို run ရမလဲဆိုတော့ 
```
go run helloword.go
```
ဆိုပြီး run လို့်ရပါတယ်။ အဲ့ဒါမှ မဟုတ်လဲနောက်တစ်နည်းက module ဆောက်ပြီး run တာပါ။ 

```
go mod int xxxxx
```
go.mod ဆိုပြီး ဆောက်သွားပါလိမ့်မယ် အဲ့ဒါဆို 

```
go run
```

ဆိုတာနဲ့ run လို့ ရနိုင်ပါတယ်။ 

Next - [Start with Helloworld](Helloworld.md)
