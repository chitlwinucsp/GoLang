## Return and handle an error
'error' library ကို import ချပါတယ်။ 

```
package main

import (
	"errors"
	"log"
)

func getStringLength(s string) (int, error) {
	if s == "" || len(s) == 0 {
		return 0, errors.New("Empty string")
	}

	return len(s), nil
}

func main() {

	log.SetPrefix("greetings: ")
	log.SetFlags(0)

	strValLen, err := getStringLength("Hello, World!")

	if err != nil {
		log.Fatal(err)
	}

	log.Println("String length : ", strValLen)

	strValLen, err = getStringLength("")
	if err != nil {
		log.Println(err)
	}

	log.Println("End of main")
}

```

errors.New("") ဆိုပြီး return ပြန်လိုက်ရင် ခေါ်သုံးတဲ့ဘက်မှာ error ပါမပါကို သိနိုင်တယ်
