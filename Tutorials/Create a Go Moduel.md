အောက်ပါအတိုင်း Module တစ်ခုကို အရင်ဆောက်မယ်။ Module ဆောက်တဲ့အခါ အရေးကြီးတာက ကိုယ် export ပေးချင်တဲ့ method ကို အကြီးနဲ့ စရေးဖို့်ပါ။

```
package greetings

import "fmt"

// Hello returns a greeting for the named person.
func Hello(name string) string {
    // Return a greeting that embeds the name in a message.
    message := fmt.Sprintf("Hi, %v. Welcome!", name)
    return message
}
```

အဲ့မှာ သတိထားမိတာ ရှိလား။ := ဆိုတာ Go language မှာက declare and initializing ရဲ့ အတိုကောက်ဖြစ်ပါတယ်တဲ့။
အရှည်သာရေးမယ်ဆို 

```
 var message string
 message = fmt.Sprintf("Hi, %v. Welcome!", name)
```
Sprintf ဆိုတာ %v ကို substitute လုပ်ပြီး print ထုတ်မယ်ပြောတာပါ။ 

နာမည်တစ်ခုနဲ့ ဖိုင်ကို save လိုက်မယ်။

```
+ tutorial (folder)
   |-- greetings/                 <-- example.com/greetings
   |-- hello/
```

greeting package ကို ဒီလိုမျိုး build  ပါမယ်။ => go mod init example.com/greetings

အဲ့ဒီ greeting ကို အခြား helloworld ဆိုတဲ့ ဖိုင်ကနေ ပြန်ခေါ်သုံးချင်တယ်ဆိုပါတော့။ 

```
    import (
         "golang.org/x/net/html" <--- External package referenced by URL
         "fmt"
         "net/http"
    )

```

Complete code be like 
```
package main

import (
    "fmt"
    "example.com/greetings"
)

func main() {
    // Get a greeting message and print it.
    message := greetings.Hello("Gladys")
    fmt.Println(message)
}
```




အဲ့မတိုင်ခင် hello folder အောက်မှာ ဒီဟာကို run ပေးဖို့လို့ပါတယ်။ 
=> go mod init example.com/hello
=> go mod edit -replace example.com/greetings=../greetings

အခြား publich package ကို ယူသုံးရင်တော့ go get ဆိုပြီး download ဆွဲလိုက်ရင် ရတယ် အခု ကျွန်တော်တို့က local package ကိုဘဲ link မှာဆိုတော့ လိုအပ်တာကို replace လုပ်ပေးလိုက်ရင် ရပါတယ်။

ပြီးသွားရင် => go mod tidy ဆိုတာ run ပေးလိုက်ပါ။ 

နောက်ဆုံး output ကို ကြည့်ချင်တယ်ဆို 
=> go run . [or] go run .\hello.go



