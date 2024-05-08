# True notation
Description of the notation for entities in the code.  
The main purpose is to be used in the GoLang code.  

***Information:***  
The name stands for "The really universal entity notation".  

***Note:***  
This naming system is not a standard.  
This system is a kind of Hungarian notation and is convenient for its author, but you can also use it if you want.  
This notation makes the code more readable, which means it simplifies application development.  
The use of this notation is solely your choice.  

***Warning:***  
Using this notation in the early stages requires self-discipline from the developer.  

## Application

- This naming system assumes that a prefix indicating the type of entity will be used before the names of entities in the code. 
- The prefix can be combined, that is, it can consist of several prefixes. 
- After the prefix, the name of the variable should be logical and correspond to its purpose. 
- There should be no spaces, hyphens, or underscores between prefixes and words. 
- Each new word or part of the prefix in the name must begin with a capital letter. 
- Constants can be named in a different style, to make them more different from ordinary entities. 
- The fields of the structure do not need to be formatted, but it is possible to use prefixes, since the insides of the structure should be understandable by themselves. 
- Prefixes in the names of functions and methods should be used as necessary, but without fanaticism, and preferably not at all. An example of reasonable usage: IsError(), IsStored(). 
- Both prefixes and postfixes can be used in naming variables and other entities. 

## The prefixes

Prefixes are placed at the beginning of the entity name and indicate its type or purpose.

### Basic data types

|Private|Public or combined|Description|Example|
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

### Aggregate and other complex data types

|Private|Public or combined|Description|Example|
|:-|:-|:-|:-|
|st|St|struct|``` var stName TUser = TUser{} ```|
|in|In|interface|``` var inAny = interface{} ```|
|sl|Sl|slice|``` var slNums = []int{} ```|
|ar|Ar|array|``` var arNums = [4]int{0, 1, 2, 3} ```|
|m|M|map|``` var mUsers = map[string]TUser ```|

### Naming types

|Private|Public or combined|Description|Example|
|:-|:-|:-|:-|
|t|T|for custom type|``` type TUser struct{} ```|

### Code entities with a special purpose

|Private|Public or combined|Description|Example|
|:-|:-|:-|:-|
|g|G|Global variables|``` var gConfig TConfig ```|
|cl|Cl|Closure variables|``` var clCount int = 0```|
|fn|Fn|Variables for storing functions and other higher-order operations|``` fnFilter := func(data uint) bool {return data/2 == 0} ```|
|d|D|The difference between the values (delta)|``` dInterval := dtSecond.Sub(dtFirst) ```|

### Entities with a frequently used purpose

|Private|Public or combined|Description|Example|
|:-|:-|:-|:-|
|f|F|For file descriptors|``` fOutput, _ := os.OpenFile(sName, os.O_CREATE, 0666) ```|
|io|Io|Types for data input and output|``` var IoFile *os.File ```|
|mx|Mx|Mutex and other blocking|``` var mxSystemBlock sync.RWMutex ```|
|at|At|Atomic|``` var atOperation atomic.Value ```|
|buf|Buf|Any buffer| |
|em|Em|Embedded data blocks|``` var emUiStaticDir embed.FS ```|
|err|Err|Errors|``` errRead := error.New("reading error") ```|
|ctx|Ctx|Sending cancellation signals|``` ctxBase := context.Background() ```|
|j|J|Encoded JSON in string|``` jText, _ := json.Marshal(&stMyRecord) ```|
|je|Je|*json.Encoder|``` jeEncoder := json.NewEncoder(f) ```|
|jd|Jd|*json.Decoder|``` jdDecoder := json.NewDecoder(f) ```|
|bs|Bs|Encoded base64 in string|``` bsText := base64.StdEncoding.EncodeToString(bData) ```|
|ch|Ch|Channels|``` var chStopSignal = make(chan struct{}, 1) ```|
|label| |Labels in the code|``` labelCheck: ```|

### A combination of prefixes

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

## The postfixes

- The postfixes are at the end of the name of a variable or other entity and show the specifics of using this entity. 
- Postfixes always start with a capital letter. 

|Postfix|Description|
|:-|:-|
|In|Input values.|
|Out|Output values.|
|It|The value of the iteration.|
|Ind|An index in an array or slice.|
|Key|An aggregate type key, for example, a key in a hash table.|
|Val|An aggregate type value, such as the value in a hash table.|

## About the author

The author of the project is Constantine Zavezeon (Kwynto).  
You can contact the author by e-mail: kwynto@mail.ru  
The author accepts proposals for participation in open source projects,  
as well as willing to accept job offers.
If you want to offer me a job, then first I ask you to read [this](https://github.com/Kwynto/Kwynto/blob/main/offer.md).
