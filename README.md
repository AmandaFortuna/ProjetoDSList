# 🎮**Projeto DSList**
Este é um projeto backend em linguagem Java desenvolvido com SpringBoot. A aplicação é uma API RESTful para gerenciamento de um catálogo de jogos, com a criação de listas personalizadas e a reordenação de jogos via endpoints. O projeto é uma prática e estudo parte do curso da DevSuperior.

## **Tecnologias utilizadas:**
- Java 17/21
- Spring Boot
- Spring Web (REST APIs)
- H2 Database
- PostgreSQL com Docker
- PGAdmin
  
## **Funções:**
- Lista de jogos
- Separação de jogos por categoria de lista
- Reordenação de títulos nas listas
- Endpoints
  
## **Driagrama:**
![WhatsApp Image 2025-08-21 at 15 38 47](https://github.com/user-attachments/assets/c0dc51ef-b97f-43db-9ecf-162cb7b60502)

## 📁**Estrutura**
```bash
   dslist/  
     ├──src/  
        ├── main/  
        │   ├── java/  
        │   │   └── com.devsuperior.dslist  
        │   │        ├── config/           -> Config da aplicação  
        │   │        ├── controllers/      -> Controle REST  
        │   │        ├── dto/  
        │   │        ├── entities/         -> entidades JPA (GameList)  
        │   │        ├── projections/      -> interface get  
        │   │        ├── repositories/     -> interfaces JPA (Integer newPosition)  
        │   │        └── services/         -> Lógica do reposicionamento  
        │   └── resources/  
        │       ├── application.properties  
        │       └── import.sql  
   ├──Mavem Dependencies/  
   ├──src/  
    ── pom.xml  
```
## 📌**Endpoints**

![1755699990678](https://github.com/user-attachments/assets/20ad3c64-34ec-4189-8fd3-e5766228c678)

- `GET /games`  
retorna a lista de todos os jogos  
```bash
[  
  {  
    "id": 1,  
    "title": "The Witcher 3",  
    "platform": "PC"  
  }  
]
```  

- `GET /games/{id}`  
retorna todas informações do jogo pelo id  
```bash
[  
  {  
    "id": 1,  
    "title": "The Witcher 3",  
    "year": 2015,  
    "genre": "RPG",  
    "platform": "PC",  
    "score": 9.5,  
    "imgUrl": "...",  
    "shortDescription": "...",  
    "longDescription": "..."  
  }  
]  
```
- `GET /lists`  
retorna todas listas de jogos  
```bash
[  
  {  
    "id": 1,  
    "name": "Favoritos"  
  }  
]`  
```
| Parâmetro | Tipo |  
|---|---|  
| id | Long |  

- `POST /lists/{listId}/replacement`  
reposiciona o jogo numa lista  
```bash
{  
  "sourceIndex": 1,  
  "destinationIndex": 3  
}  
```
| Parâmetro | Tipo |  
|---|---|  
| ReplacementDTO | Integer |  

## 🙋Autora

Amanda Fortuna dos Santos  
www.linkedin.com/in/amanda-fortuna-4401a614a  
