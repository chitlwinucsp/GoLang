**Program** တိုင်းဟာ package နဲ့စတယ်။

Import fmt, math/rand က သုံးမဲ့ package ကို declare လုပ်တာဖြစ်တယ်။

အခြား language တွေလိုဘဲ program တိုင်းဟာ main နဲ့စပါတယ်။

```

package main

import (
	"fmt"
	"math/rand"
)

func main() {
	fmt.Println("My favorite number is", rand.Intn(10))
}

```

import ကို တစ်ကြောင်းချင်းစီရေးလဲရပါတယ်တဲ့ ။ ဒါပေမဲ့ အပေါ်ကလို ရေးတာကတော့ ပိုကောင်းတာပေါ့နော်။ 

```
import "fmt"
import "math"
```

နောက်တစ်ခုက **Exported names** ပဲ။ Capital letter နဲ့ စရေးထားတဲ့ဟာတွေက exported name ဖြစ်တယ်။

နမူနာ - 

```
package main

import (
	"fmt"
	"math"
)

func main() {
	fmt.Println(math.pi)
}

```

အပေါ်က code ကို run ရင်သေချာပေါက် error တက်မှာဖြစ်တယ်။ pi ဆိုတာကို မသိနေဘူး။ အမှန်က Pi ပဲဖြစ်ရမှာပါ။ (``` ./prog.go:9:19: undefined: math.pi ```)
အဲ့ဒါအပြင်ကို အစပထမပုဒ်က println ကို ကြည့်ရင်လဲ သိနိုင်ပါတယ် package ထဲက ပေးထားတဲ့ method တွေကို ခေါ်သုံးခွင့်ပေးချင်ရင် နာမည်ကို capital letter ကို စရေးရမှာဖြစ်ပါတယ်။

**Functions** 
အဲ့ဒါကလဲ အထူးအဆန်းတော့ မဟုတ်ပါဘူး အခြား programming language တွေလိုဘဲ parameters(arguments) တွေက zero or more နဲ့ ရေးလို့ရနိုင်တယ်။

```
func add(x int, y int) int {
	return x + y
}
```

အပေါ်ကဟာက ထူးခြားနေတာ မဟုတ်ပေမဲ့ ဆန်းသစ်တဲ့ဟာက parameter မှာ two or more တွေရဲ့ ဘေးချင်ကပ် type တွေက တူနေတယ်ဆိုရင် အဲ့ဒါကို အဆုံးမှာ ထုတ်ရေးလို့ရတယ်တဲ့။
ဒီတစ်ခုကတော့ ထူးခြားတာပေါ့နော်။

```
func add(x, y int) int {
	return x + y
}
```

**Function Return**
function return ကလဲ နည်းနည်းထူးခြားတယ်။ အပေါ်က add ဆိုတဲ့ method မှာ return တစ်ခုပေါ့နော်။
result အများကြီးကိုလဲ ပြန်လို့ရပါတယ်တဲ့။

```
package main

import "fmt"

func swap(x, y string) (string, string) {
	return y, x
}

func main() {
	a, b := swap("hello", "world")
	fmt.Println(a, b)
}

```

```
Output : world hello
```

function တွေအကြောင်းသာ ပြောနေတယ် အရေးကြီးတဲ့ structure အကြောင်းကို လေ့လာကြည့်ရအောင်

![function structure image](https://go.dev/doc/tutorial/images/function-syntax.png)

Next - [Create a Go Module](Create%20a%20Go%20Moduel.md)

