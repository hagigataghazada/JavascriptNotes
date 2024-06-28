
# JAVASCRIPT
Javascript 3 müxtəlif yolla web səhifəyə əlavə olunur: 

  **1. Inline**

  **2. Internal**

  **3. External**

## Inline
Inline Javascript onclick və ya onload kimi attributlardan istifadə edərək birbaşa HTML elementi daxilinə Javascript kodunun yerləşdirilməsi deməkdir.  
Məsələn, 
```
<button onclick="alert('Salam, Dünya!')">Mənə Klikləyin</button>
```
Burada onclick attributundan istifadə olunub. Düyməni kliklədikdə atribut daxilindəki Javascript kodu işə salınır, "Salam, Dünya" mesajı ilə xəbərdarlıq göstərilir. Başqa bir nümunə:
```
<!DOCTYPE html >
<html>
<head>
   <h2> This is a simple HTML file</h2>
   <script>
      document.write("Hi, This is an inline Javascript code written in between script tags");
   </script>
</head>
</html>
```
**Inline Javascriptin üstünlükləri:**

Tətbiqi asandır. Çünki ayrıca script tag-ləri və xarici fayllar (external files) tələb etmir. Dərhal istifadəçi hərəkətlərinə(user actions) cavab verir, geridönüş(feedback) edir. 

**İnline Javascriptin dezavantajları:**

Bu zaman Javascript kodu birbaşa HTML elementinə daxil etdiyi üçün kod bazası böyüdükcə onu saxlamaq və idarə etmək çətinləşə bilər. 

## Internal

Internal Javascript Javascript kodunun HTML sənədində ```<script>``` tag-indən istifadə edərək yerləşdirilməsinə aiddir. Kod birbaşa HTML faylı daxilində, adətən ```<head>``` və ya ```<body>``` bölməsində yazılır.

**Internal Javascriptin üstünlükləri:**

Javascript kodunu birbaşa HTML faylının içərisinə  daxil edib,  yazmağı və  başa düşməyi asanlaşdırır. Daxili Javascript kodu HTML sənədindəki digər elementlər üçün əlçatandır. Bu da qüsursuz qarşılıqlı əlaqəyə imkan verir. Brauzer əlavə **HTTP**  sorğuları etmədən Javascript kodunu yükləyə və icra edə bilər. Nəticədə daha sürətli performans təmin edilir. 

**Internal Javascriptin dezavantajları:**

Daxili Javascript kodu birdən çox  HTML faylı arasında asanlıqla təkrar edilə bilməz. Kodun təkrarlanmasna səbəb olur. Kod bazası böyüdükcə HTML faylları daxilində daxili Javascript-i idarə etmək və yeniləmək çətinləşə bilər. 

```
<html>
<head>
  <title>Internal JavaScript Example</title>
  <script>
    function greet() {
      console.log('Hello, World!');
    }
  </scrip>
</head>
<body>
  <button onclick="greet()">Click Me</button>
</body>
</html>
```
## External

External Javascript Javascript kodunu .js uzantılı ayrı-ayrı xarici fayllarda saxlamağa və ```<script>``` tag-inin **src** attributundan istifadə edərək HTML sənədinə əlaqələndirməyi nəzərdə tutur. Javascript kodunu ayrı-ayrı fayllarda saxlamaqla kodun təşkili və narahatlıqların bərpasını asanlaşdırır. 

**External Javascriptin üstünlükləri:**

Xarici JS faylları çoxlu HTML faylları arasında təkrar istifadə oluna bilər. Kodun təkrarını azaldır. Xarici Javascript fayllarını idarə etmək və yeniləmək daha asandır. Çünki onlar HTML strukturundan asılı olmadan dəyişdirilə bilər. Brauzerlər xarici Javascript fayllarını saxlaya bilər və nəticədə web sayta sonrakı ziyarətlər üçün daha sürətli yükləmə vaxtları olur.

**External Javascriptin dezavantajları:**

Çoxsaylı External Javascript fayllarının yüklənməsi əlavə HTTP sorğuları ilə nəticələnə bilər.  Bu da ilkin  səhifə yükləmə vaxtına təsir edir. 

```
<html>
<head>
  <title>External JavaScript Example</title>
  <script src="script.js"></scrip>
</head>
<body>
  <!-- HTML content goes here -->
</body>
</html>
```
# **Javascript Code Structure**

## Statements(Codes)

Statement verilən bir təlimatdır. Statement nöqtəli vergüllə **";"(semicolon)** sonlandırılır. Bir sətrə çoxlu sayda statement-lar yaza bilərsiniz. Lakin daha oxunaqlı olması üçün her statement-in bir sətirdə yerləşməsi lazımdır. 

```
// bu oxumaq üçün daha asandır
console.log("Hello!");
console.log("Hi!");
console.log("Hallo!");
// bu oxumaq üçün daha çətin
console.log("Hello!");
console.log("Hi!");
console.log("Hallo!");
```

Javascriptdə statement-lar value, operator, keyword, comment-dən  ibarətdir. 

Statement-lar Javascript hərəkətini müəyyən etmək üçün **keyword**-lərlə başlayır. keyword-lərə misal  olaraq **let, var, const, if, for, function** göstərmək olar.

## Operators

Operatorlar(operators) toplama, çıxma, vurma, bölmə kimi əməliyyatlara icazə verən dəyərlər arasındakı simvollardır. Operatorların tipləri:

1. Arithmetic Operators
2. Assignment Operators
3. Comparison(Relational) Operators
4. Logical Operators
5. Unary Operators
6. Ternary(Conditional) Operators
7. Special Oprators

### Arithmetic Operators

1. `"+"` - addition
2. `"-"` - substraction
3. `"*"` - multiplication
4. `"/"` - division
5. `"%"` - modulus(remainder)
6. `"**"` - exponential
```
let num1 = 10;
let num2 = 20;
let num3 = num1 + num2;
console.log(num3);

let m = "Hello";
let n = "World!";
let a = m + n;
console.log(a); //Output: HelloWorld!
```

### Assignment Operators

1. `"="` (assign)  -  x=y same as "x=y"

2. `"+="` (add and assign) - x+=y same as "x=x+y"

3. `"-="` (substract and assign) - x-=y same as "x=x-y"

4. `"*="` (multiply and assign) - x*=y same as "x=x*y"

5. `"/="` (divide and assign) - x/=y same as "x=x/y"

6. `"%="` (modulus and assign) - x%=y same as "x=x%y"

7. `**= ` (exponent and assign) - x**=y same as "x=x**y"

```
let x = 10;
x += 5; // x = x + 5

let x = 10;
x -= 5; // x = x - 5
```

### Comparison(Relational) Operators

1. `"=="` - equal in value only
2. `"==="` - equal in value and data type
3. `"!="` - not equal to
4. `"!=="` - not identical
5. `">"` - greater than
6. `">="` - greater than or equal to
7. `"<"` - less than
8. `"<="` - less than or equal

```
console.log(15<25); //Output : true
console.log(3 != 2); //Output : true
console.log(3 != 3); //Output : false
``` 

### Logical Operators

1. `"&&"` - logical and, ampersand
2. `"||"` - logical or, pipe
3. `"!"` - logical not, negation

```
const check = 4>3 && 10>5; //true && true = true
const check = 4>3 && 5>10; //true && false = false
const check = 4<1 && 5>10; //false && false = false

const check = 4>3 || 10>5; //true || true = true
const check = 4>3 || 5>10; //true || false = true
const check = 4<1 || 5>10; //false || false = false

let check = 4>3; //true
let check = !(4>3); //false
```
### Unary Operators

1. Unary Minus (-)
2. Increment (++)
3. Decrement (--)
4. Addressof operator ( & )
5. Sizeof()

#### Unary Minus

Arqumentin, dəyərin işarəsini dəyişir. Pozitiv rəqəm neqativə, neqativ rəqəm pozitivə çevrilir. Minus (-) operatoru substraction (çıxma) operatorundan fərqlidir. Substraction operatoru iki dəyər tələb edir.

```
let m = 10;
let n = -m;
console.log(n); //Output: -10
```

#### Increment Operator  

1. Pre-increment (prefix)
```
let num1 = 10;
console.log(num1); //10
console.log(++num1); //11

let num2 = 5;
let num3 = ++num2;
console.log(num3); //6
```
2. Post-increment (postfix)
```
let num1 = 10;
console.log(num1++); //10
console.log(num1); //11
```

####  Decrement Operator

1. Pre-decrement 
```
let num1 = 10;
console.log(num1); //10
console.log(--num1); //9
console.log(--num1); //8

let num2 = 5;
console.log(--num2); //4
console.log(num2); //4

let num3 = 5;
let num4 = --num3;
console.log(num4); //4
```
2. Post-decrement
```
let num1 = 10;
console.log(num1); //10
console.log(num1--); //10
console.log(num1); //9

let num2 = 5;
console.log(num2--); //5
console.log(num2); //4
```

### Ternary Operators

Ternary Operators vəziyyət, şərt yaratmağa icazə verir.

```
let isRaining = true
isRaining
  ? console.log('You need a rain coat.') //Output
  : console.log('No need for a rain coat.')

isRaining = false
isRaining
  ? console.log('You need a rain coat.')
  : console.log('No need for a rain coat.') // Output
```

```
let number = 3
number > 0
  ? console.log(`${number} is a positive number`) //Output
  : console.log(`${number} is a negative number`)

number = -1
number > 0
  ? console.log(`${number} is a positive number`)
  : console.log(`${number} is a negative number`) //Output
```

### Special Operators

1. `"'?',':'"` - ternary, conditional operators
2.  `","` - comma operator
3. `"delete"` operator
4. `"in"`
5. `"intanceof"`
6. `"new"`
7. `"typeof"`
8. `"void"`
9. `"yield"`


## Delete Operator
Delete operatoru obyektdən property (dəyişəni) silir.

```
let person = {
  name: "John",
  age: 25,
  city: "Baku"
};
console.log(person); //Output { name: 'John', age: 25, city: 'Baku' }
delete person.age;
console.log(person); //Output { name: 'John', city: 'Baku' }
```
## In Operator

In operatoru seçilmiş property-in (xüsusiyyət) seçilmiş obyektdə və ya onun prototipində olub-olmadığını yoxlayır. 
```
const car = {make: 'Honda', model: 'Accord', year: 1998};
console.log('make' in car); //Output: true
delete car.make;
if ('make' in car === false) {
  car.make = 'Suzuki';
}
console.log(car.make);
```

## Typeof Operator 

Dəyərin tipini qaytarır.

```
let num = 10;
let str = "Hello";
let bool = true;
let und = undefined;
console.log(typeof num); // Output: number
console.log(typeof str); // Output: string
console.log(typeof bool); // Output: boolean
console.log(typeof und); // Output: undefined
```

## Operator Presedence (Operator Üstünlüyü)

Üstünlüyü daha yüksək olan operatorlar üstünlüyü aşağı olan operatorların operandlarına çevrilirlər. 

```
console.log(5 + 10 * 2); //5 + 20 = 25
console.log(5 + 10 / 2); //5 + 5 = 10
console.log(4 * 3 ** 2); //4 * 9 = 36
```

## Variables (Dəyişənlər)
 
Variables (dəyişənlər) dataları saxlamaq üçün istifadə olunur. Dəyişənləri təyin etmək üçün let, var, const açar sözlərindən (keywords) istifadə olunur.  Dəyişənlərə qiymət təyin etmək üçün **" = " - equal sign** (assignment operator) istifadə olunur.

```
let x;
x = 6;
let x = 6;
```
Burada **let** dəyişən təyin etmək üçün keyword (açar söz), **x**-variable (dəyişən), **6**-value(dəyər)dir. Biz dəyişənə verdiyimiz dəyəri istədiyimiz qədər dəyişə bilərik. Məsələn, 

```
let message
message = "Hello!"

message = "Hi!" //value changed

message = "Hallo!" //value changed
```

Dəyər dəyişdikdə köhnə data dəyişəndən silinir. Biz eyni zamanda iki dəyişən təyin edib, datanı birindən digərinə kopyalaya bilərik. Məsələn, 

```
let hello = "Hello!"
let hi
hi = hello

console.log(hello)
console.log(hi)
```
Eyni dəyişəni ikinci dəfə təyin etmək xətaya səbəb olur. Məsələn, 

```
let message = "Hello!"
let  message = "Hi!" //Syntax error: Identifier 'message' has already been declared

```
Dəyişən adları yalnız hərflər, rəqəmlər, "_"-alt cizgi (underscore) və dollar işarəsi (dollar sign) $-dan ibarət ola bilər. Məsələn, ```message```, ```message_1```, ```message1```, ```_message```, ```message_```, ```_message_1```
Dəyişənin adında 1-ci xarakter rəqəm ola bilməz. ```message_1``` doğru, ```1_message``` doğru deyil. ```console```, ```let```, ```function``` kimi ayrılmış açar sözlərdən dəyişən təyin etmək üçün istifadə edə bilməzsiniz. Çünki bunlar Javascript tərəfindən müəyyən təlimatları yerinə yetirmək üçün istifadə olunur.Javascript case-sensitive, yəni böyük/kiçik hərflərə həssas bir dildir. ```Message```, ```MESSAGE```, ```message``` 3 müxtəlif dəyişən yaratmaq üçün istifadə oluna bilər. Lakin bu cür dəyişən adları yaratmaq tövsiyə olunmur.

```
//Correct Variable names 
let $ = 1
let _ = 2
let myNameIs = "Anar"
//Incorrect Variable names
let 1name = "Anar"
let my-name-is = "Anar"
```
 Bəzən dəyişən təyin etmək üçün 1 sözdən daha çoxuna ehtiyac olur. Javascriptdə bütün dünyada istifadə olunan iki adlandırma konvensiyası vardır:

1. camelCase 
2. snake_case

**camelCase** - sonrakı hər sözün ilk hərfi böyüklə yazılır. Məsələn, 

```
let myNameIs
```
**snake_case** - bu adlandırma konvensiyasında sözləri ayırmaq üçün alt xətdən (underscore "_") istifadə olunur. 

```
let my_name_is
``` 
**Constant Variable (dəyişməyən dəyər)** - dəyərini dəyişməyən dəyişəndir. Sabit dəyişən **const** açar sözündən istifadə edilərək təyin edilir. 

```
const pi = 3.14
```
Sabit dəyərlər dəyişdirilə bilməz, yenidən təyin edilə bilməz.

```
const myAge = 24
myAge = 25 //error
```

```
var myAge = 24
```
## Comments

Kodların nə etdiyini açıqlayan comment-lərin əlavə edilməsi lazımlıdır. **Tək sətirli comment-lər (single line comment)** iki slash **" // "** işarəsi ilə yazılır. Məsələn,

```
// Home Section Starts
```
**Çox sətirli comment-lər (multiline comment)** ***" / * "** başlayır, **" * / "*** ilə bitir. Məsələn,

```
 /* This is multiline comment

    for example  */ 
```

Yazdığınız yanlış və ya artıq sizə lazım olmayan hissəni də **comment** vasitəsilə delete istifadə etmədən yox edə bilərsiniz. Çünki Comment-lər dil prosessoru tərəfindən nəzərə alınmır, göz ardı edilir. Dil prosessoru kodları yuxarıdan-aşağıya oxuyur. Birinci sətirdə yazılan kod ikincidən əvvəl yerinə yetiriləcək.

```
console.log("Hi!");
//console.log("false code or not important code");
```

Qısayol: ` ctrl +  / `

# Data Types (Data Tipləri)

Dataların və dəyərlərin data tipləri vardır. Data tipləri dataların xüsusiyyətlərini təsvir edir. Data tipləri **primitive** və **non-primitive (Object References)** olmaqla iki yerə ayrılır.

## Primitive Data Tipləri

1. String
2. Number
3. Boolean
4. Undefined
5. Null
6. Symbol

Primitiv data tipləri **non-modifiable (immutable)** yəni dəyişdirilə bilməzlər.

```
let m = "Hello!";
// əgər stringi dəyişməyə çalışsaq, Javascript xəta(error) verəcək.
m[0] = "A";
//yəni 0-cı yerdə duran (indeksi 0 olan) elementi ("H"), "A" ilə dəyişməyə çalişsaq
```

###   Strings

Bir və ya bir neçə xarakterdən ibarət olub, **double quotes (qoşa dırnaqlar) ""**, **single quotes (tək dırnaqlar) ''**, **backticks (tərs dırnaqlar) ``** arasında yazılır.

```
'a'
"Hello!"
'World'
`We can also use backstick`
```

#### String birləşdirmə 

Stringləri birləşdirməyin müxtəlif yolları vardır. Bunlardan biri addition operatorundan istifade etməklə :

```
let firstName = "John"; 
let lastName = "Doe"; 
let fullName = firstName + " " + lastName; 
console.log(fullName); // "John Doe"
```

Stringlər bir xarakterdən, paraqraf və ya səhifədən ibarət ola bilər. Əgər stringin uzunluğu çoxdursa və bir sətrə yerləşmirsə bu zaman hər sətrin sonuna backslash / qoyuruq və stringin sonrakı sətrdə davam edəcəyini bildiririk. 

```
const paragaraph = "My name is John Doe. I live in Berlin, Germany. I am 25 years old. I study at California State University. /
My profession is Doctor. My family consist of 5 people: my father, mother, sister, brother and me. My father is doctor too. /
```

**Escape Sequences in Strings**

1. **`\n`** - new line
2. **`\t`** - tab, means 8 spaces
3. **`\\`** - back slash
4. **`\'`** - single quote
5. **`\"`** - double quote

```
let name = prompt('Ad daxil edin');
console.log(`Hello ${name} necesen?`);
```

#### String Methods

1. ***length*** - Boşluq daxil xarakterlərin sayını,  deyişənin uzunluğunu göstərir. 

```
let name = 'John';
console.log(name.length); //Output: 4
```

2. ***Index*** - String-dəki xarakterləri əldə etmək üçün ***index***-dən istifadə olunur. index 0-dan başlayır. stringdəki 1-ci xarakterin indeksi 0-dır. Sonuncu indeks "length - 1"-ə bərabərdir. 

```
let string = 'Trust';
let firstLetter = string[0];
console.log(firstLetter); //Output: t
let secondLetter = string[1];
console.log(secondLetter); //Output: r
let lastIndex = string.length - 1;
console.log(lastIndex); //Output: 4
console.log(string[lastIndex]); //Output: t
```

3. ***toUpperCase()*** - bu metod stringi böyük hərflə yazdırır.

```
let string = 'John';
console.log(string.toUpperCase()); //JOHN
```

4. ***toLowerCase()*** - bu metod stringi kiçik hərflə yazdırır.

```
let string = 'JOHN';
console.log(string.toLowercase()); //john
```

5. ***substr()*** - Iki arqument alır, başlanğıc indeksi və bölünən xarakterlərin sayı. 

```
let string = 'butterfly';
console.log(string.substr(6, 3)); //fly   (yəni 6-dan başla 3-nü böl/götür)
```

6. ***substring()*** - Iki arqument alır, başlanğıc indeksi və dayanma indeksi. Lakin dayanma indeksindəki xarakter daxil deyil. 

```
let string = 'butterfly';
console.log(string.substring(0, 6)); //butter  (yəni, 0-dan başla 6-ya çatanda dayan/6-cı daxil deyil)
console.log(string.substring(6)); //fly  (burada isə başlanğıc indeksi 6 bildirilib, lakin dayanma indeksi bildirilmiyib bu zaman 6-dan
başlayaraq 6-dan sonrakıları götürür/bölür)
console.log(string.substring(6, 9)); //fly (burada isə dayanma indeksi 9 bildirilib çünki 8 yazsaq dayanma indeksi daxil olmadığından 
sonuncu indeksdəki elementi götürməyəcək, 9 yazırıq ki, 8-ci indeksi götürsün)
```

7. ***split()*** - stringi müəyyən edilmiş yerdə bölür.

```
let string = '30 Days Of Javascript';
console.log(string.split()); // Array-e çevirir. ["30 Days Of Javascript"]
console.log(string.split(' ')); // boşluqda bölür. ["30", "Days", "Of", "Javascript"]

let firstName = 'John';
console.log(firstName.split('')); // hərf-hərf bölür. ["J", "o", "h", "n"]

let countries = 'Azerbaijan, Turkey, Russia, Georgia, Iran';
console.log(countries.split(',')); //Array daxilindəki elementləri vergüllə bölür. ["Azerbaijan", "Turkey", "Russia", "Georgia", "Iran"]
```

8. ***trim()*** - Başlanğıcda və sonda olan boşluqları silir.

```
let string = ' Hello ';
console.log(string.trim()); //Hello   
//və ya
console.log(string.trim(' '));
```

9. ***includes()*** - Elementin string daxilində olub-olmadığını yoxlayır. Bu metod boolean qaytarır. Əgər element stringdə varsa, true, yoxdursa false qaytarır. 

```
let string = '30 Days Of Javascript';
console.log(string.includes('Days')); // true
console.log(string.includes('days')); // false (caseSensitive olduğundan false qaytarır)
let country = 'Azerbaijan';
console.log(country.includes('a')); //false (caseSensitive olduğundan false qaytarır)
```

10. ***replace()*** - iki parametr alır: 
string.replace(oldsubstring(əvəz ediləcək element(köhnə)), newsubstring (əvəz olunduğu element(yeni)))

```
let string = '30 Days Of Javascript';
console.log(string.replace('Javascript', 'Python')); // 30 Days Of Python 
```

11. ***charAt()*** - index götürür və həmin index-dəki dəyəri(elementi) qaytarır.

```
let string = '30 Days Of Javascript';
console.log(string.charAt(0)); // 3
```

12. ***charCodeAt()*** - index götürür və həmin index-dəki dəyərin ASCII nömrəsini qaytarır. 

```
let string = '30 Days Of Javascript';
console.log(string.charCodeAt(3)); // D ASCII - 68
```

13. ***indexOf()*** -  elementin string daxilində olub-olmadığını yoxlayır və əgər varsa hemin elementin birincisinin index-ni qaytarır, yoxdursa -1 qaytarır. 

```
let string = '30 Days Of Javascript';
console.log(string.indexOf('Days')); // 3
console.log(string.indexOf('days')); // -1
```

14. ***lastIndexOf()*** - elementin string daxilində olub-olmadığını yoxlayır və əgər varsa həmin elementin sonuncusunun index-ni qaytarır, yoxdursa -1 qaytarır.

```
let string = '30 Days Of Javascript';
console.log(string.lastIndexOf('a')); // 14
```

15. ***concat()*** - çoxlu elementləri alıb onları birləşdirir.

```
let string = '30';
console.log(string.concat(' Days', ' Of', ' Javascript')); // 30 Days Of Javascript
```

16. ***startsWith*** - bir substringi arqument olaraq alır və stringin həmin arqumentlə başlayıb başlamadığını yoxlayır. Boolean qaytarır.

```
let string = '30 Days Of Javascript';
console.log(string.startsWith('30')); // true
```

17. ***endsWith*** - bir substringi arqument olaraq alır və stringin həmin arqumentlə bitib-bitmədiyini yoxlayır. Boolean qaytarır.

```
let string = '30 Days Of Javascript';
console.log(string.endsWith('Javascript')); // true
```

18. ***search*** - bir substringi və ya RegEx arqument olaraq alır və həmin arqumentlə ilk uyğunlaşanın index-ni qaytarır. 

```
let string = '30 Days Of Javascript';
console.log(string.search('Days')); // 3
```

19. ***match*** - bir arqumentin (string və ya RegEx) stringdəki elementlərlə uyğunluğunu yoxlayır. Əgər uyğunlaşma varsa array qaytarır, yoxdursa null qaytarır. 

```
let string = 'I love Javascript. If you do not love Javascript what else can you love.';
console.log(string.match('love')); //['love', index: 2, input: 'I love Javascript. If you do not love Javascript what else can you love.', groups: undefined]
```
```
let pattern = /love/gi; // g bütün mətndə axtarılması deməkdir. i - case insensitive 
console.log(string.match(pattern))   // ["love", "love", "love"]
```

20. ***repeat*** - arqument olaraq ədəd alır və stringin o qədər də təkraralanmış  halını qaytarır.

```
let string = 'Day';
console.log(string.repeat(2)); // DayDay
```

#### Data tiplərinin dəyişdirilməsi (Casting)

Bir data tipini başqa bir data tipinə dəyişmək mümkündür. Bu zaman **parseInt(), parseFloat(), Number(), +sign, str()** metodlarından  istifadə edirik. 

#### String to Int 
Biz string number-ı number-a çevirə bilərik. Dırnaq içərisində hər hansı integer number string number-dır. String number-a '2' '10' və s. misal göstərmək olar. String number-ı number-a bu metodlarla çevirə bilərik: **parseInt(), Number(), + sign**. 

```
let number = '5';
let numInteger = parseInt(number);
console.log(numInteger); //5

let num = '5';
let numberInt = Number(num);
console.log(numberInt);  //5

let num = '5';
let numInt = +num;
console.log(numberInt); //5

```

#### String to Float
String float number-ı float number-a çevirə bilərik. Dırnaq içərisində yazılan hər hansı float number string number-dır. String float number-a '2.4', '5,6'  və s. misal göstərmək olar. String float number-ı float number-a bu metodlarla çevirmək olar: **parseFloat(), Number(), + sign**. 

```
let num = '5,5';
let numToFloat = parseFloat();
console.log(numToFloat);

let number =  '6,7';
let numFloat = Number(number);
console.log(numFloat);

let num = '6,5';
let numFloat = +num;
console.log(numFloat);
```

#### Float to Int 
Float number-ı Integer-a çevirmək üçün **parseInt()** metodundan istifadə edirik.

```
let num = 9.81;
let numInt = parseInt(num);
console.log(numInt); //9
```

### Numbers

Integers: mənfi(negative), 0(zero), müsbət(positive) ədədlər 
Float-point: -3.5, -1.0, 1.1, 2.2 və s.

```
let number = 10;
console.log(number); // 10
let floatNum = 2,5;
console.log(floatNum); // 2.5
```

### Math Object 

Math Objectin ədədlərlə işləmək üçün çoxlu metodları vardır. 

**Math.round** - ədədləri yuvarlaqlaşdırmaq üçün istifadə olunur. 

```
let a = 5.5;
console.log(Math.round(a)); // 6
let b = 3.3;
console.log(Math.round(b)); // 3
```

**Math.floor** - ədədləri kiçiyə doğru yuvarlaqlaşdırır. 

```
let a = 3.6;
console.log(Math.floor(a)); // 3
```
**Math.ceil** - ədədləri böyüyə doğru yuvarlaqlaşdırır. 

```
let a = 3.3;
console.log(Math.ceil(a)); // 4
```

**Math.min** - Minimum dəyəri qaytarır.

```
console.log(Math.min(-2, 3, 4, -5)); // -5
```
**Math.max** - Maximum dəyəri qaytarır.

```
console.log(Math.max(-5, 5, 14, 1)); // 14
```
### Random Number Generator

**Math.random** - konsola random ədəd çıxarır.
```
const randomNumber = Math.random(); // 0 və 0.999999 arasında rəqəm çıxarır. 
console.log(randomNumber); 
```
```
let randomNum = Math.random(); 
let numZeroToTen = randomNum * 11;
console.log(numZeroToTen); // min 0 və max 10.99 arasında random ədəd verir.
```
```
const num = Math.floor(Math.random() * 11); //konsola 0 və 10 arasında random ədəd çıxarır.
console.log(num); // min 0 max 10 arasında random ədəd verir.  
```

### Boolean 

Boolean true və ya false dəyərlərini qaytarır. 
0, On, undefined, null, Nan, " " false dəyərini qaytarır.

```
let trueValue = 5 < 10;
console.log(trueValue); // true

let falseValue = 2 > 12;
console.log(falseValue); // false
```

#### Her zaman true dəyərlər

**bütün ədədlər (pozitiv və neqativ ədədlər), 0 daxil deyil**

**bütün stringlər (boş string daxil deyil(''))**

**true dəyəri**

#### Hər zaman false dəyərlər

**0**

**0n**

**null**

**undefined**

**NaN**

**false dəyəri**

**'', "", ``**

### Undefined 

Eger biz dəyişənə(variable) dəyər(value) vermiriksə, dəyər(value) **undefined** olur. 

```
let name;
console.log(name); // undefined
```

### Null 

Null (empty value or no value) boş dəyər deməkdir. 

```
let name = null;
console.log(name); // null
```

### Symbol

Simvol konstruktoru tərəfindən yaradıla bilən unikal dəyərdir.

## Window Methods

Window alert() method - bu metod müəyyən mesaj və OK düyməsi olan xəbədarlıq qutusu göstərir. 

```
alert(message);

alert("Hello World!");

```
Window prompt() method - bu metod iki arqument alır. İkinci arqument istəyə bağlıdır. Dəyər qəbul edən sorğu qutusudur.

```
prompt('required text', 'optional text');
let number = prompt('enter a number');
console.log(number);

```

Window confirm() method - bu metod müəyyən mesaj, OK və Cancel düymələri olan dialoq qutusunu göstərir. 

```
confirm('required text');
let answer = confirm('Are you sure?');
console.log(answer);
```

## Data Objects



## Non-Primitive Data Tipləri

Non-primitiv data tipləri **modifiable(mutable)**, yəni dəyişdirilə bilən data tipləridir.

1. Array
2. Object

Məsələn, aşağıdakı array-de dəyərlərdən birini dəyişək
```
let numbers = [1, 2, 3];
numbers[1] = 5;
console.log(numbers); // [1, 5, 3]
```

Non-primitive data tipləri dəyərlərinə görə müqayisə edilə bilməz. (hətta bu data tipləri eyni xüsusiyyətlərə və dəyərlərə malik olasalar belə ) 

```
let nums = [1, 2, 3];
let numbers = [1, 2, 3];
cosole.log(nums == numbers); //false

let personOne = {
  name: 'Jony',
  job: 'teacher'
}
let personTwo = {
  name: 'Jony',
  job: 'teacher'
}
console.log(personOne == personTwo); //false
```

Onlar referans yerlərinə görə  müqayisə edilir. İki obyekt  eyni obyektı istinad etdikdı bərabır olurlar.

```
let personOne = {
  name: 'Jony',
  job: 'teacher'
}
let personTwo = personOne;
console.log(personOne == personTwo); //true
```

### Array bax!!!!

Array kvadrat mötərizədə (square bracket) yerləşən data dəyərlərdən ibarətdir. Arrayler eyni və ya müxtəlif data tiplərindən ibarət ola bilər. Array dəyərlərinə onların indeksi ilə istinad edilir. İndeks 0-dan başlayır. Arrayin 1-ci elementinin indeksi 0, 2-ci elementin indeksi 1 və s. bu kimi davam edir. 

```
let arr = [1, 2, 3, 4, 5];
console.log(arr[0]); // 1
console.log(arr[1]); // 2
arr[0] = 5;
console.log(arr); // [5, 2, 3, 4, 5]
```


# Higher Order Function

Higher Order Function-lar başqa bir funksiyanı parametr olaraq götürən yaxud bir funksiyanı dəyər olaraq qaytaran funksiyalardır.

### Callback

Parametr olaraq götürülən funksiya callback funksiya adlanır.

```
const callback = (m) => {
    console.log(m);
}
const higherOrder = (callback) => {
    callback("Hello World");
}

higherOrder(callback);
```
### Returning Function 
Higher Order Function-lar funksiyanı dəyər olaraq qaytarır. 

```
const highOrder = (n) => {
  const  newOrder = (m) => {
    const changeOrder = (l) => {
      return n + m + l
    }
    return changeOrder
  }
  return newOrder
}
console.log(highOrder(2)(3)(4))
```

# Document Object Model (DOM)

 HTML sənədi Javascript obyekti olaraq strukturlaşdırılmışdır. Hər HTML elementinin onu dəyişdirən xüsusiyyətləri vardır. Javascript istifadə edərək HTML elementlərini **get(almaq), create(yaratmaq), append(əlavə etmək), remove(silmək)** mümkündür. Javascript istifadə edərək HTML elementlərinin seçilməsi CSS istifadə etməklə seçilməyə bənzəyir. HTML elementini seçmək üçün biz  **tag adlarından, id, class adları və digər attributlardan** istifadə olunur.

 ## Getting Element (Element almaq)
 Biz yaradılmış elementə və ya elementlərə Javascript vasitəsilə əldə edə bilərik. Bu elementləri əldə etmək və ya almaq üçün müxtəlif metodlardan istifadə olunur. 
 ```
 <!DOCTYPE html>
  <html lang="en">
    <head>
      <title>Document Object Model<title>
    </head>
    <body>
      <h1 class='title' id='first-title'>First Title</h1>
      <h1 class='title' id='second-title'>Second Title</h1>
      <h1 class='title' id='third-title'>Third Title</h1>
      <h1></h1>
    </body>
  </html>
```

### Getting elements by tag name 

 ***getElementsByTagName()*** - tag adını string parametri kimi götürür. Bu metod HTML Collection Obyekti qaytarır. HTML Collection HTML elementləri obyekti kimi arraydir. length xüsusiyyəti (property) HTML Collection ölçüsünü göstərir. Bu metoddan istifadə etməklə biz hər bir elementi index və ya for loopundan istifadə edərək əldə edirik. HTML Collection bütün array metodlarını dəstəkləmir, ona görə də biz forEach əvəzinə for loopundan iistifadəə etməliyik. 
 ```
document.getElementsByTagName('tagname')
```
```
const allTitles = document.getElementsByTagName('h1')
console.log(allTitles) // HTMLCollection(4) [h1, h1, h1, h1]
console.log(allTitles.length) // 4
for (let i = 0; i < allTitles.length; i++) {
  console.log(allTitles[i]) // h1, h1, h1, h1
}
```

### Getting elements by class name
***getElementsByClassName()*** - HTML Collection obyekti qaytarır. 
```
document.getElementsByClassName('classname')
```
```
const allTitles1 = document.getElementsByClassName('title')
console.log(allTitles1) // HTMLCollection(3) [h1, h1, h1]
console.log(allTitles1.length) //3
for (let i = 0; i < allTitles1.length; i++) {
  console.log(allTitles1[i]) // h1, h1, h1
}
```

### Getting an element by id
***getElementById()*** - tək HTML elementini hədəfləyir. 
```
document.getElementById('id')
```
```
let firstTitle = document.getElementById('first-title')
console.log(firstTitle) // <h1 id="first-title">First Title</h1>
```

### Getting elements by using querySelector methods
***document.querySelector*** - metodu bir və ya bir çox HTML elementlərini tag name, id və classname - ə görə seçə bilər. 

***querySelector*** - HTML elementlərini tagname və ya classlarına görə seçir. Əgər tagname və class istifadə olunursa, o, ilk elementi seçir.
```
let first_Title = document.querySelector('h1');
console.log(first_Title); // <h1 id="first-title">First Title</h1>
let firstTitle1 = document.querySelector('.title');
console.log(firstTitle1); // <h1 class="title">First Title</h1>
let firstTitle2 = document.querySelector('#first-title');
console.log(firstTitle2); // <h1 id="first-title">First Title</h1>
```

***querySelectorAll*** - HTML elementlərini  onların tagname və classlarına görə seçir. nodeList qaytarır. Hər nodeList elementləri arasında dövr etmək üçün for loop və ya forEach istifadə edə bilərik.
```
const allTitles = document.querySelectorAll('h1') //səhifədəki bütün h1 elementlərini seçir. 
console.log(allTitles); // NodeList(4) [h1, h1, h1, h1]
console.log(allTitles.length); // 4
for (let i = 0; i < allTitles.length; i++) {
  console.log(allTitles[i])
}
allTitles.forEach(title => console.log(title))
const allTitles11 = document.querySelectorAll('.title')
console.log(allTitles11); // NodeList(3) [h1, h1, h1]
```
### Adding attribute/without setAttribute
HTML tag-lərinə element haqqında əlavə məlumat verən attributlar əlavə olunur. Ən çox istifadə olunan HTML attributları: id, class, src, style, href, disabled, title, alt. 

```
const title8 = document.querySelectorAll('h1')
title8[3].className = 'title'
title8[3].id = 'fourth-title'
```

### Adding attribute using setAttribute
***setAttribute()*** - bu metod istƏnilən HTML attributunu təyin edir. İki parametr alır: attributun tipi(növü) və attributun adı. 
```
const titles = document.querySelector('h1')
titles[3].setAttribute('class', 'title')
titles[3].setAttribute('id', 'fourth-title')
```

### Adding class using classList
***classList*** - metodu əlavə class əlavə edir. Class varsa original class-ı ləğv etmir, əksinə element üçün əlavə class əlavə edir. 

```
titles[3].classList.add('title', 'header-title')
```
### Removing class using remove
***classList.remove*** - biz bu metodla elementdən class-ı silə bilərik.

```
  titles[3].classList.remove('title', 'header-title')
```
### Adding text to HTML element 
Biz elementə **textContent** və ya **innerHTML** istifadə etməklə mətn məzmunu(text content) əlavə edə bilərik. 
 
#### Using textContent 
***textContent*** property - HTML elementinə mətn əlavə etmək üçün istifadə olunur. 
```
const titles = document.querySelectorAll('h1')
titles[3].textContent = 'Fourth Title'
```
#### Using innerHTML
***innerHTML*** property - biz valideyn(parent) elementi əvəz etmək və ya tamamilə yeni uşaq məzmunu əlavə etmək üçün istifadə olunur. 
```
<!DOCTYPE html>
<html lang="en">
  <head>
    <title>DOM</title>
  </head>
  <body>
    <div class="wrapper">
      <h1>30 Days</h1>
      <h2>Javascript</h2>
      <ul></ul>
    </div>
    <script>
      const lists = `
      <li>30DaysOfJavascript</li>
      <li>30DaysOfJavascript</li>
      <li>30DaysOfJavascript</li>
      <li>30DaysOfJavascript</li>
      <li>30DaysOfJavascript</li>`
      const ul = document.querySelector('ul')
      ul.innerHTML = lists
    </script>
  </body>
</html>
```

**innerHTML** həmçinin child elementləri parent elementindən silə bilir. 
```
const ul = document.querySelector("ul");
ul.innerHTML = '';
```
### Adding style
#### Adding style color 

```
const titles = document.querySelectorAll('h1')
titles.forEach((title, i) => {
  title.style.fontSize = '24px' //bütün title-larda font-size 24px olacaq
  if (i % 2 === 0) {
    title.style.color = 'green'
  } else {
    title.style.color = 'red'
  }
})
// və ya 
for (let i = 0; i < titles.length; i++) {
  const title = titles[i];
  title.style.fontSize = '24px'; //bütün title-larda font-size 24px olacaq
  if (i % 2 === 0) {
    title.style.color = 'green';
  } else {
    title.style.color = 'red';
  }
}
```
#### Adding style background color 
```
const titles = document.querySelectorAll('h1')
titles.forEach((title, i) => {
  if (i % 2 === 0) {
    title.style.backgroundColor = 'green'
  } else {
    title.style.backgroundColor = 'blue'
  }
})
for (let i = 0; i<titles.length; i++){
  const title = titles[i]
  if (i % 2 === 0) {
    title.style.backgroundColor = 'green'
  } else {
    title.style.backgroundColor = 'blue'
  }
}
```
### Creating an element/elements

***document.createElement('tagname')***
```
<!DOCTYPE html>
<html>
<head>
  <title>Document Object Model</title>
</head>
<body>
  <script>
    let title = document.createElement('h1')
    title.className = 'title'
    title.style.fontSize = '25px'
    title.textContent = 'DOM Day 2'
  </script>
</body>
</html>
```
Çoxlu elementlər yaratmaü üçün biz loop(döngü) istofadə edirik. Loop vaasitəsilə biz istədiyimiz qəqdər element yarada bilərik. 
```
<!DOCTYPE html>
<html>
<head>
  <title>Document Object Model</title>
</head>
<body>
  <script>
    let title
    for (let i = 0; i<4; i++){
      title = document.createElement('h1')
      title.className = 'title'
      title.style.fontSize = '25px'
      title.textContent = i
      console.log(title)
    }
  </script>
</body>
</html>
```
### Appending child to a parent element 
Yaradılmış elementi görmək üçün biz onu parent(valideyn) elementə child(uşaq) element kimi əlavə etməliyik. HTML sənədində body-ye biz document.body ilə əldə edirik. document.body appendChild() metodunu dəstəkləyir.
