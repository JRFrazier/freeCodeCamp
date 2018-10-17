---
title: Error Handling
localeTitle: Обработка ошибок
---
# Обработка исключений на C ++

Исключением является проблема, возникающая во время выполнения программы. Исключения обеспечивают способ передачи управления из одной части программы в другую. Обработка исключений C ++ построена на трех ключевых словах: #try, #catch и #throw.

*   # throw - программа выдает исключение, когда возникает проблема. Это делается с использованием ключевого слова throw.
    
*   # catch - программа выхватывает исключение с обработчиком исключений в месте в программе, где вы хотите справиться с этой проблемой. Ключевое слово catch указывает на улавливание исключения.
    
*   #try - блок try идентифицирует блок кода, для которого будут активированы определенные исключения. За ним следует один или несколько блоков catch.
    

```CPP
#include <iostream> 
 using namespace std; 
 
 int main() 
 { 
   int x = -1; 
 
   // Some code 
   cout << "Before try \n"; 
   try { 
      cout << "Inside try \n"; 
      if (x < 0) 
      { 
         throw x; 
         cout << "After throw (Never executed) \n"; 
      } 
   } 
   catch (int x ) { 
      cout << "Exception Caught \n"; 
   } 
 
   cout << "After catch (Will be executed) \n"; 
   return 0; 
 } 
```

# Прежде чем продолжить ...

## Обзор

*   Группировка типов ошибок.
*   Разделение кода обработки ошибок из нормального кода.
*   Функции / методы могут обрабатывать любые исключения, которые они выбирают.