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
   |-- greetings/
   |-- hello/
```

အဲ့ဒီ greeting ကို အခြား helloworld ဆိုတဲ့ ဖိုင်ကနေ ပြန်ခေါ်သုံးချင်တယ်ဆိုပါတော့။ 

