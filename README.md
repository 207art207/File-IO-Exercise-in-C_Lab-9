# Навігація по документу
- [Вправа 1](#завдання)
- [Компіляція коду](#компіляція-коду)

## Завдання: 
Написати програму, яка яка створює файл у форматі
markdown і записує у цей файл деякий список гіперпосилань. Список
гіперпосилань для кожного із варіантів приведений у таблиці нище.

![список_гіперпосилань](https://github.com/207art207/Informatika_Lab9/blob/main/task.png?raw=true)
```
 #include <stdio.h>

int main() {
    
    FILE *file = fopen("Lab_9_result.md", "w"); // Відкриваємо (створюємо) файл "Lab_9_result.md" для запису

    
    if (file != NULL) {
        
        fprintf(file, "# Список гіперпосилань:\n\n"); // Записуємо заголовок у файл

        
        fprintf(file, "- [Вибіркові дисципліни](http://its.kpi.ua/uk/node/234)\n");
        fprintf(file, "- [Перелік освітніх компонент](http://its.kpi.ua/uk/node/266)\n");
        fprintf(file, "- [Зразки основних документів](http://its.kpi.ua/uk/node/146)\n"); // Записуємо гіперпосилання у файл

        
        fclose(file); // Закриваємо файл

        
        printf("The file was successfully created.\n"); // Виводимо повідомлення про успішне створення файлу
    } else {
        
        printf("Error.\n"); // Виводимо повідомлення про невдале створення файлу
    } // Перевіряємо, чи вдалося відкрити файл

    return 0;
}
```
## Компіляція коду
![Компіляція коду](https://github.com/207art207/Informatika_Lab9/blob/main/Compilation_of_code.png?raw=true)
![Результат](https://github.com/207art207/Informatika_Lab9/blob/main/Result.png?raw=true)
