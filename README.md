# highload-art-gallery

**Предметная область**: система для картинной галереи, продажи билетов на выставки и хранения данных о коллекции
* Связь "многие-ко-многим" между пользователями и ролями, и между галереей и картинами


```mermaid
    classDiagram

    user "*" -- "*" role
    user "1" -- "*" order
    order "1" -- "*" ticket
    gallery "1" -- "*" ticket
    exhibition "1" -- "*" ticket
    exhibition "*" -- "1" gallery
    gallery "*" -- "*"  painting
    painting "*" -- "1" style
    painting "*" -- "1" artist

```


Архитектура базы данных:

![](doc/hl1.jpg)