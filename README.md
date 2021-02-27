# adyen-footsites
---

Adyen Encryption for footsites, only v18 - you can add other versions yourself :)

---


Example:
```Go
package main

import (
	y "github.com/awxsam/adyen-footsites"
)
func main() {
	adyenKey := "Public Adyen Key"
	y := y.NewAdyen(adyenKey)
	encryptedCCNumber,encryptedExpMonth, encryptedExpYear, encryptedCvc := y.EncryptCreditcardDetails("CCNUMBER", "EXPMONTH", "EXPYEAR", "CVC")
	fmt.Println(encryptedCCNumber)
	fmt.Println(encryptedExpMonth)
	fmt.Println(encryptedExpYear)
	fmt.Println(encryptedCvc)
}
