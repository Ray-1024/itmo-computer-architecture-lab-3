### Отчёт

* Сковородников Дмитрий Алексеевич
* Группа: P33111
* `lisp | cisc | harv | mc | tick | struct | stream | mem | pstr | prob5`

### Пояснение

* Язык программирование: `lisp` (Синтаксис языка Lisp. S-exp)
* Архитектура: `cisc` (Система команд должна содержать сложные инструкции)
* Организация памяти: `harv` (Гарвардская архитектура )
* Control Unit: `mc` (Микрокод)
* Точность модели: `tick` (Процессор необходимо моделировать с точностью до такта, процесс моделирования может быть приостановлен на любом такте)
* Представление машинного кода: `struct` (В виде высокоуровневой структуры данных. Считается, что одна инструкция укладывается в одно машинное слово, за исключением CISC архитектур)
* Ввод-вывод: `stream` (Ввод-вывод осуществляется как поток токенов)
* Ввод-вывод ISA: `mem` (memory-mapped (порты ввода-вывода отображаются в память и доступ к ним осуществляется штатными командами))
* Тип строк: `pstr` (Length-prefixed (Pascal string))
* Алгоритм: `prob5` ([Smallest multiple](https://projecteuler.net/problem=5))

### Язык программирования

* Описание синтаксиса (в форме Бэкуса-Наура)
```text
    <program> ::= <statement> | <statement> <program>
    
    <statement> ::= <common_statement> | <function_definition>
    
    <common_statement> ::= '(' <statement_name> <statement_args> ')'
    
    <statement_name> ::= <identifier> | <math_operation> | <boolean_operation>
    <identifier> ::= 
    <math_operation> ::= '+' | '-' | '*' | '/'
    <boolean_operation> ::= '=' | '>'
    
    <statement_args> ::= 
    
    <literal> ::= <integer> | <string>
    
    <integer> ::= ["-"] <unsigned_integer>    
    <unsigned_integer> ::= <digit> | <non_zero_digit> <digit> | <non_zero_digit> <digit> <unsigned_int>
    <digit> ::= "0" | <non_zero_digit>
    <non_zero_digit> ::= '1' | '2' | '3' | '4' | '5' | '6' | '7' | '8' | '9'
    
    <string> ::= '"' <string_chars> '"'
    <string_chars> ::= <any symbol except '"'>
     
    
```

* Семантика
  * Стратегия вычислений
  * Области видимости
  * Типизация и виды литералов