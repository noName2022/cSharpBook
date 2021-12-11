---
description: Особенности языка программирования
---

# Синтаксис

#### Первая программа приветствия на экране

```csharp

using System; // Подключенное пространство имен.
              // В новых версиях VS начальные пространства имен скрыты.    


namespace HelloWorld   // Объявление нового пространства имен
{
    
    class Program      // Объявление нового класса
    { 
        
        static void Main(string[] args) // Объявление нового метода
        {
            Console.WriteLine("Hello, world!"); // Вывод на экран текста
            Console.ReadKey(); // Ожидание ввода
            
        }      // Окончание метода
    
    }     // Окончание объявление нового класса
    
}    // Окончание объявления нового пространства имен

```

#### Комментарий

```
// Это однострочный комментарий
/* Это многострочный 
     комментарий */    
```

#### Переменные

Синтаксис объявления переменных в C# выглядит следующим образом:

_<mark style="color:orange;">`<Тип данных>`</mark>        <mark style="color:blue;">`<Идентификатор>`</mark>   _    <mark style="color:red;">`;`</mark>

<mark style="color:red;">``</mark>

Например:

```csharp
int integer;
float speed;
string myName;

int numberOne, numberTwo, numberThree;  // Обьявление нескольких переменных одновременно
```

_Все переменные в C# должны быть объявлены до их применения_

Наименование переменных чувствительны к регистру

__

### Инициализация переменной

Задать значение переменной можно, в частности, с помощью оператора присваивания: __ `=` .

Пример:&#x20;

```csharp
int i = 10;        
/// задаем целочисленной переменной i значение 10
char symbol = 'Z';  
 // инициализируем переменную symbol буквенным значением Z
float f = 15.7F;  
 // переменная f инициализируется числовым значением 15.7
int x = 5, y = 10, z = 12;
int numberOne = 1, numberTwo = 2, numberThree = 3;    
// инициализируем несколько переменных одного типа
var i = 12;     // переменная i инициализируется целочисленным литералом
var d = 12.3;   // переменная d инициализируется литералом с плавающей точкой,
                // имеющему тип double
var f = 0.34F;  // переменная f теперь имеет тип float
```



### Набор встроенных типов данных <a href="#set-intrinsic-data-types" id="set-intrinsic-data-types"></a>

В следующей таблице показываются поддерживаемые [типы данных](https://docs.microsoft.com/ru-ru/office/vba/language/glossary/vbe-glossary#data-type), включая размеры хранилищ и диапазоны.

| Тип данных                                                                                                                                                                                                   | Размер хранилища                                                             | Диапазон                                                                                                                                                                                                                               |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ---------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [**Boolean**](https://docs.microsoft.com/ru-ru/office/vba/language/reference/user-interface-help/boolean-data-type)                                                                                          | 2 байта                                                                      | **True** или **False**                                                                                                                                                                                                                 |
| [**Byte**](https://docs.microsoft.com/ru-ru/office/vba/language/reference/user-interface-help/byte-data-type)                                                                                                | 1 байт                                                                       | от 0 до 255                                                                                                                                                                                                                            |
| **Collection**                                                                                                                                                                                               | Неизвестно                                                                   | Неизвестно                                                                                                                                                                                                                             |
| [**Currency**](https://docs.microsoft.com/ru-ru/office/vba/language/reference/user-interface-help/currency-data-type) (масштабируемое целое число)                                                           | 8 байт                                                                       | от –922 337 203 685 477,5808 до 922 337 203 685 477,5807                                                                                                                                                                               |
| [**Date**](https://docs.microsoft.com/ru-ru/office/vba/language/reference/user-interface-help/date-data-type)                                                                                                | 8 байт                                                                       | от 1 января 100 г. до 31 декабря 9999 г.                                                                                                                                                                                               |
| [**Decimal**](https://docs.microsoft.com/ru-ru/office/vba/language/reference/user-interface-help/decimal-data-type)                                                                                          | 14 байт                                                                      | <p>+/–79 228 162 514 264 337 593 543 950 335 без десятичной запятой<br><br>+/–7,9228162514264337593543950335 с 28 разрядами справа от десятичной запятой<br><br>Наименьшее ненулевое число равно +/–0,0000000000000000000000000001</p> |
| **Dictionary**                                                                                                                                                                                               | Неизвестно                                                                   | Неизвестно                                                                                                                                                                                                                             |
| [**Double**](https://docs.microsoft.com/ru-ru/office/vba/language/reference/user-interface-help/double-data-type) (число с плавающей запятой двойной точности)                                               | 8 байт                                                                       | <p>от –1,79769313486231E308 до –4,94065645841247E-324 для отрицательных значений<br><br>от 4,94065645841247E-324 до 1,79769313486232E308 для положительных значений</p>                                                                |
| [**Integer**](https://docs.microsoft.com/ru-ru/office/vba/language/reference/user-interface-help/integer-data-type)                                                                                          | 2 байта                                                                      | от –32 768 до 32 767                                                                                                                                                                                                                   |
| [**Long**](https://docs.microsoft.com/ru-ru/office/vba/language/reference/user-interface-help/long-data-type) (целое число Long)                                                                             | 4 байта                                                                      | от –2 147 483 648 до 2 147 483 647                                                                                                                                                                                                     |
| [**LongLong**](https://docs.microsoft.com/ru-ru/office/vba/language/reference/user-interface-help/longlong-data-type) (целое число LongLong)                                                                 | 8 байт                                                                       | <p>от –9 223 372 036 854 775 808 до 9 223 372 036 854 775 807<br><br>Действительно только для 64-разрядных платформ.</p>                                                                                                               |
| [**LongPtr**](https://docs.microsoft.com/ru-ru/office/vba/language/reference/user-interface-help/longptr-data-type) (целое число Long в 32-разрядных системах, целое число LongLong в 64-разрядных системах) | <p>4 байта в 32-разрядных системах<br><br>8 байт в 64-разрядных системах</p> | <p>от –2 147 483 648 до 2 147 483 647 в 32-разрядных системах<br><br>от –9 223 372 036 854 775 808 до 9 223 372 036 854 775 807 в 64-разрядных системах</p>                                                                            |
| [**Object**](https://docs.microsoft.com/ru-ru/office/vba/language/reference/user-interface-help/object-data-type)                                                                                            | 4 байта                                                                      | Любая ссылка на **Object**                                                                                                                                                                                                             |
| [**Single**](https://docs.microsoft.com/ru-ru/office/vba/language/reference/user-interface-help/single-data-type) (число с плавающей запятой одинарной точности)                                             | 4 байта                                                                      | <p>от –3,402823E38 до –1,401298E-45 для отрицательных значений<br><br>от 1,401298E-45 до 3,402823E38 для положительных значений</p>                                                                                                    |
| [**String**](https://docs.microsoft.com/ru-ru/office/vba/language/reference/user-interface-help/string-data-type) (переменная длина)                                                                         | 10 байтов + длина строки                                                     | от 0 до приблизительно 2 миллиардов                                                                                                                                                                                                    |
| **String** (фиксированная длина)                                                                                                                                                                             | Длина строки                                                                 | от 1 до приблизительно 65 400                                                                                                                                                                                                          |
| [**Variant**](https://docs.microsoft.com/ru-ru/office/vba/language/reference/user-interface-help/variant-data-type) (с числами)                                                                              | 16 байт                                                                      | Любое числовое значение до диапазона типа **Double**                                                                                                                                                                                   |
| **Variant** (с символами)                                                                                                                                                                                    | 22 байта + длина строки (24 байтов в 64-разрядных системах)                  | Тот же диапазон как для типа **String** переменной длины                                                                                                                                                                               |
| [**Определяется пользователем**](https://docs.microsoft.com/ru-ru/office/vba/language/how-to/user-defined-data-type) (используя **Type**)                                                                    | Число, необходимое для элементов                                             | Диапазон каждого элемента совпадает с диапазоном его типа данных.                                                                                                                                                                      |



### Проверка типов данных <a href="#verify-data-types" id="verify-data-types"></a>

Чтобы проверить типы данных, ознакомьтесь с приведенными ниже функциями.

* [IsArray](https://docs.microsoft.com/ru-ru/office/vba/language/reference/user-interface-help/isarray-function)
* [IsDate](https://docs.microsoft.com/ru-ru/office/vba/language/reference/user-interface-help/isdate-function)
* [IsEmpty](https://docs.microsoft.com/ru-ru/office/vba/language/reference/user-interface-help/isempty-function)
* [IsError](https://docs.microsoft.com/ru-ru/office/vba/language/reference/user-interface-help/iserror-function)
* [IsMissing](https://docs.microsoft.com/ru-ru/office/vba/language/reference/user-interface-help/ismissing-function)
* [IsNull](https://docs.microsoft.com/ru-ru/office/vba/language/reference/user-interface-help/isnull-function)
* [IsNumeric](https://docs.microsoft.com/ru-ru/office/vba/language/reference/user-interface-help/isnumeric-function)
* [IsObject](https://docs.microsoft.com/ru-ru/office/vba/language/reference/user-interface-help/isobject-function)

### Возвращаемые значения функции CStr

| Если _expression_                                                                         | CStr возвращает                                                                                                                               |
| ----------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------- |
| **Boolean**                                                                               | Строка, содержащая значение **True** или **False**.                                                                                           |
| **Date**                                                                                  | Строка, содержащая полный или краткий формат даты, установленный в системе.                                                                   |
| [Empty](https://docs.microsoft.com/ru-ru/office/vba/language/glossary/vbe-glossary#empty) | Строка нулевой длины ("").                                                                                                                    |
| **Error**                                                                                 | Строка, содержащая слово **Error** и [номер ошибки](https://docs.microsoft.com/ru-ru/office/vba/language/glossary/vbe-glossary#error-number). |
| [Null](https://docs.microsoft.com/ru-ru/office/vba/language/glossary/vbe-glossary#null)   | [Ошибка во время выполнения](https://docs.microsoft.com/ru-ru/office/vba/language/glossary/vbe-glossary#run-time-error).                      |
| Другое числовое значение                                                                  | Строка, содержащая число                                                                                                                      |











