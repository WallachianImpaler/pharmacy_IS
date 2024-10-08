﻿# Информационная система аптеки
 
# 1. Постановка задачи

## 1.1 Тема задачи и предметная область

Вариант 15. Тема: «Информационная система аптеки»

## 1.2 Описание предметной области и требования к базе данных
Аптека продает медикаменты и изготавливает их по рецептам. Лекарства могут быть разных типов:

1. Готовые лекарства: таблетки, мази, настойки: 
2. Изготовляемые аптекой: микстуры, мази, растворы, настойки, порошки 

Различие в типах лекарств отражается в различном наборе атрибутов, их характеризующих. Микстуры и порошки изготавливаются только для внутреннего применения, растворы для наружного, внутреннего применения и для смешивания с другими лекарствами и мази только для наружного применения. Лекарства различны также по способу приготовления и по времени приготовления. Порошки и мази изготавливаются смешиванием различных компонент. При изготовлении растворов и микстур ингредиенты не только смешивают, но и отстаивают с последующей фильтрацией лекарства, что увеличивает время изготовления.

В аптеке существует справочник технологий приготовления различных лекарств. В нем указываются: идентификационный номер технологии, название лекарства и сам способ приготовления. На складе на все медикаменты устанавливается критическая норма, т.е. когда какого-либо вещества на складе меньше критической нормы, то составляются заявки на данные вещества и их в срочном порядке привозят с оптовых складов медикаментов.

Для изготовления аптекой лекарства больной должен принести рецепт от лечащего врача. В рецепте должно быть указано: ФИО, подпись и печать врача, ФИО, возраст и диагноз пациента, также количество лекарства и способ применения. Больной отдает рецепт регистратору, он принимает заказ и смотрит, есть ли компоненты заказываемого лекарства. Если не все компоненты имеются в наличии, то делает заявки на оптовые склады лекарств и фиксирует ФИО, телефон и адрес не обслуженного покупателя, чтобы сообщить ему, когда доставят нужные компоненты. Такой больной пополняет справочник заказов - это те заказы, которые находятся в процессе приготовления, с пометкой, что не все компоненты есть для заказа. Если все компоненты имеются, то они резервируются для лекарства больного. Покупатель выплачивает цену лекарства, ему возвращается рецепт с пометкой о времени изготовления. Больной также пополняет справочник заказов в производстве. В назначенное время больной приходит и по тому же рецепту получает готовое лекарство. Такой больной пополняет список отданных заказов.

Ведется статистика по объемам используемых медикаментов. Через определенный промежуток времени производится инвентаризация склада. Это делается для того, чтобы определить, есть ли лекарства с критической нормой, или вышел срок хранения или недостача.

Виды запросов в информационной системе:

1. Сведения о покупателях, которые не пришли забрать свой заказ в назначенное им время и общее их число;
2. Перечень и общее число покупателей, которые ждут прибытия на склад нужных им медикаментов в целом и по указанной категории медикаментов;
3. Перечень десяти наиболее часто используемых медикаментов в целом и указанной категории медикаментов;
4. Какой объем указанных веществ использован за указанный период;
5. Перечень и общее число покупателей, заказывавших определенное лекарство или определенные типы лекарств за данный период;
6. Перечень и типы лекарств, достигших своей критической нормы или закончившихся;
7. Перечень лекарств с минимальным запасом на складе в целом и по указанной категории медикаментов;
8. Полный перечень и общее число заказов находящихся в производстве;
9. Полный перечень и общее число препаратов требующихся для заказов, находящихся в производстве;
10. Все технологии приготовления лекарств указанных типов, конкретных лекарств, лекарств, находящихся в справочнике заказов в производстве;
11. Сведения о ценах на указанное лекарство в готовом виде, об объеме и ценах на все компоненты, требующиеся для этого лекарства;
12. Сведения о наиболее часто делающих заказы клиентах на медикаменты определенного типа, на конкретные медикаменты;
13. Сведения о конкретном лекарстве (его тип, способ приготовления, названия всех компонент, цены, его количество на складе).
 
Целью создания информационной системы является автоматизация процессов, происходящих в фармацевтической компании.

# 2. Моделирование базы данных

## 2.1. Схема ER-модели

![pharmacyER](https://github.com/user-attachments/assets/d27ce89a-53a9-420d-a3c1-3aecdbe946b5)
