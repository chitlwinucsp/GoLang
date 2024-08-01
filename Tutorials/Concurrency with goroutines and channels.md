## Concurrency with goroutines and channels

ဒီဟာကတော့ C# language တွေမှာဆို thread နဲ့ ဆင်တူပါတယ်။ 

parallel လုပ်ဆောင်တာမျိုးပါ။ အဲ့အတွက်ကို go keyword ကို သုံးပေးရပါမယ်။ 

```
  package main

import (
	"fmt"
	"time"
)

func count(thing string) {
	for i := 1; i <= 5; i++ {
		fmt.Println(i, thing)
		time.Sleep(time.Millisecond * 1)
	}
}

func main() {
	go count("sheep")
	count("fish")
	time.Sleep(time.Second * 1)
}

```

အဲ့မှာ time.sleep ကကျတော့ C# မှာဆို thread.sleep နဲ့တူပါတယ် ခဏ sleep ပြီး အခြားဟာကို လုပ်ပါဆိုတဲ့ သဘောပါ။ 

Output be like 
```
1 fish
1 sheep
2 fish
2 sheep
3 sheep
3 fish
4 fish
4 sheep
5 sheep
5 fish
```
