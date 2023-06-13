# Калькулятор энергосбережения.
----------------

**Описание**:  
Программа калькулятор энергопотребления, предназначена для работы с данными, связанными с именами, числами и значениями потребления. Он предоставляет методы для добавления элементов в списки и получения суммарного значения потребления.


**Скриншот рабочего окна приложения**: 

![](![image](https://github.com/LevSebelev/docs-management-course/assets/113666462/9668b7f7-4c0b-4b7a-8176-4e7d9d5a09c2)




## Зависимости
В коде нет явных зависимостей от внешних библиотек или классов. Однако, так как используются классы ArrayList и Iterator из пакета java.util, предполагается, что программа зависит от стандартной библиотеки Java.

## Установка

Для использования этого кода не требуется дополнительной установки. Он может быть скопирован и вставлен в проект на Java для дальнейшего использования.

## Применение

Служит для рассчёта потребления электричества приборами.

## Проблемы

Данная программа выполняет поставленные перед ней функции, сбоев не обнаружено.

## Получение справочной информации

По всем вопросам просьба писать по электроному адрессу: leva.sebelev@mail.ru.


## Приглашение к сотрудничеству

Все желающие могут использовать данный проект в своих целях. 
Также я не против, если кто-то внесёт свою лепту в модернизации программы.

## Open source licensing info
1. [TERMS](TERMS.md)
2. [LICENSE](LICENSE)
3. [CFPB Source Code Policy](https://github.com/cfpb/source-code-policy/)


----

## Источники и справочники
Я пользовался учебными методичками и пособиями, которые нам предоставил преподаватель, по написанию программ на Java
## Пример кода 

```Java
package model;

import java.util.ArrayList;
import java.util.Iterator;
import java.util.List;

public class kalc
{

    protected List NameSet = new ArrayList();
    protected List CountSet = new ArrayList();
    protected List PowerSet = new ArrayList();
    public String getit(int n) {
        int i = 0;
        Iterator iterator1 = NameSet.iterator();
        Iterator iterator2 = CountSet.iterator();
        Iterator iterator3= PowerSet.iterator();

