# go-notation
Description of the notation for entities in the GoLang code.

***Note:***  
*This naming system is not a standard.*  
*This system is a kind of Hungarian notation and is convenient for its author, but you can also use it if you want.*  
*This notation makes the code more readable, which means it simplifies application development.*  
*The use of this notation is solely your choice.*  

***Warning:***  
*Using this notation in the early stages requires self-discipline from the developer.*  

## Application

- This naming system assumes that a prefix indicating the type of entity will be used before the names of entities in the code. 
- The prefix can be combined, that is, it can consist of several prefixes. 
- After the prefix, the name of the variable should be logical and correspond to its purpose. 
- There should be no spaces, hyphens, or underscores between prefixes and words. 
- Each new word or part of the prefix in the name must begin with a capital letter. 
- Constants can be named in a different style, to make them more different from ordinary entities. 
- The fields of the structure do not need to be formatted, but it is possible to use prefixes, since the insides of the structure should be understandable by themselves. 

## Basic data types

|Private|Public|Description|Example|
|:-|:-|:-|:-|
|b|B|byte|``` var bText byte ```|
|r|R|rune|``` var rChar rune ```|
|s|S|string|``` var sText string ```|
|fl|Fl|float, float32, float64|``` var flNumber float ```|
|i|I|int, int8, int16, int32, int64|``` var iNumber int ```|
|u|U|uint, uint8, uint16, uint32, uint64|``` var uNumber uint ```|
|c|C|complex64, complex128|``` var cNumber complex64 ```|
|bi|Bi|BigInt|``` biNumber := new(big.Int) ```|
|is|Is|bool|``` var isOk bool ```|
|dt|Dt|Date and time|``` dtNow := time.Now() ```|
|p|P|pointer| |
|r|R|reference|``` rNow := &dtNow ```|

## Aggregate and other complex data types

|Private|Public|Description|Example|
|:-|:-|:-|:-|
|st|St|struct|``` var stName TUser = TUser{} ```|
|in|In|interface|``` var inAny = interface{} ```|
|sl|Sl|slice|``` var slNums = []int{} ```|
|ar|Ar|array|``` var arNums = [4]int{0, 1, 2, 3} ```|
|m|M|map|``` var mUsers = map[string]TUser ```|

## Naming types

|Private|Public|Description|Example|
|:-|:-|:-|:-|
|t|T|for custom type|``` type TUser struct{} ```|

## Code entities with a special purpose

|Private|Public|Description|Example|
|:-|:-|:-|:-|
|g|G|Global variables|``` var gConfig TConfig ```|
|cl|Cl|Closure variables|``` var clCount int = 0```|
|fn|Fn|Variables for storing functions and other higher-order operations|``` fnFilter := func(data uint) bool {return data/2 == 0} ```|
|d|D|The difference between the values (delta)|``` dInterval := dtSecond.Sub(dtFirst) ```|

## Entities with a frequently used purpose

|Private|Public|Description|Example|
|:-|:-|:-|:-|
|f|F|for file descriptors|``` fOutput, _ := os.OpenFile(sName, os.O_CREATE|os.O_APPEND|os.O_RDWR, 0666) ```|
|mx|Mx|mutex and other blocking|``` var mxSystemBlock sync.RWMutex ```|
|j|J|Encoded JSON in string|``` jText, _ := json.Marshal(&stMyRecord) ```|
|bs|Bs|Encoded base64 in string|``` bsText := base64.StdEncoding.EncodeToString(bData) ```|

## A combination of prefixes

|Private|Public|Description|Example|
|:-|:-|:-|:-|
|slS|SlS|slice of string|``` var slSNames []string{} ```|
|slU|SlU|slice of uint|``` var slUNumbers []uint{} ```|
|slB|SlB|slice of byte|``` var slBAscii []byte{} ```|
| | | | |
|tSl|TSl|custom slice|``` type TSlStorageUsers []TUser{} ```|
|tSt|TSt|custom struct|``` type TStResponse struct {} ```|

***Note:***  
*You can use any prefix combination order that is convenient for you or that is provided for by the code design agreement in your team.*  

## About the author

The author of the project is Constantine Zavezeon (Kwynto).  
You can contact the author by e-mail: kwynto@mail.ru  
The author accepts proposals for participation in open source projects,  
as well as willing to accept job offers.
If you want to offer me a job, then first I ask you to read [this](https://github.com/Kwynto/Kwynto/blob/main/offer.md).
