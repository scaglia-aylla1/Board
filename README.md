# Criando um Board com persistência de Dados

## Diagrama de Classes
```mermaid
classDiagram
    class Board {
        -int id
        -String name
    }

    class BoardColumn {
        -int id
        -String name
        -String kind
        -int order
    }

    class Block {
        -int id
        -String blockCause
        -String unblockCause
        -Data unblockIn
    }

    class Card {
        -int id
        -String title
        -String description
        -Data createdAt
    }

    Board --> BoardColumn
    Board --> Block
    Board --> Card


    Board "1"*--"N" BoardColumn
    Board "1"*--"N" Card
    Board "1"*--"N" Block    
```
