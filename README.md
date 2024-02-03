# Домашнее задание к занятию "Testability, авто-тесты, введение в ООП: объекты и методы"

##  Инструкция к выполнению домашнего задания

1. Скачайте и установите профессиональный редактор кода [Intellij Idea Community Version](https://www.jetbrains.com/idea/download/).
2. Откройте IDEA и [создайте новый Java-проект](QA_Java_Idea_Create.md). Под каждую задачу следует создавать отдельный проект, если обратное не сказано в условии.
3. Создайте пустой репозиторий на GitHub и свяжите его с папкой вашего проекта, а не с какой-либо другой.
4. Правильно настройте репозиторий в плане `.gitignore`. Проигнорируйте папки `.idea` и `out` и `.iml`-файл — их в репозитории быть не должно.
5. Выполните в IDEA требуемую задачу согласно условию.
6. Проверьте соблюдение [правил форматирования кода](QA_Java_Idea_Format.md).
7. Закоммитьте и отправьте в репозиторий содержимое папки проекта.

## Задание 1. Мили - модернизация (обязательное к выполнению)

Вы уже научились создавать классы и методы. Поэтому вам необходимо модернизировать приложение для рассчёта миль. Теперь сама логика рассчёта будет находиться в специально выделенном классе сервиса, а в Main мы будем лишь создавать объект этого сервиса и вызывать его метод, передавая аргументами все необходимые данные для рассчёта. Получив от вызова метода рассчитанный результат, мы выведем его на экран.

#### Этапы выполения
1. Создайте класс `BonusMilesService` (`File -> New -> Java Class`, вводите название и нажимаете `Enter`)
1. Определите в нём метод `calculate`, который:
* Принимает на вход один параметр: `cost` типа `int`
* Анализируя значение переданного параметра, возвращает рассчитанное количество миль (тип - `int`)

Разместите следующий код в классе `Main`:

```java
public class Main {
    public static void main(String[] args) {
        BonusMilesService service = new BonusMilesService();
        int price = 10_000;
        int miles = service.calculate(price);
        System.out.println(miles);
    }
}
```

Убедитесь, что выводимое в консоль значение соответствует результатам предыдущей версии приложения.

#### Правила приёма работы
Для каждой задачи прикреплена ссылка на публичный репозиторий GitHub с решением.
