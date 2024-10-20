# highload-art-gallery

**Subject Area**: Art gallery management, exhibition ticket sales, and collection data storage.

There are many-to-many relationships between users and roles, as well as between galleries and paintings.


```mermaid
   classDiagram

    class User
    class Role
    class Order
    class Ticket
    class Exhibition
    class Gallery
    class Painting
    class Style
    class Artist

    User "*" -- "*" Role
    User "1" -- "*" Order
    Order "1" -- "*" Ticket
    Exhibition "1" -- "*" Ticket
    Exhibition "*" -- "1" Gallery
    Gallery "*" -- "*" Painting
    Painting "*" -- "1" Style
    Painting "*" -- "1" Artist

```


Database Schema:

![](doc/hl1.jpg)