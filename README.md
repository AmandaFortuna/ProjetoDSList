# 🎮**Projeto DSList**
Este é um projeto backend em linguagem Java desenvolvido com SpringBoot. A aplicação é uma API RESTful para gerenciamento de um catálogo de jogos, com a criação de listas personalizadas e a reordenação de jogos via endpoints. O projeto é uma prética e estudo do curso da DevSuperior.

## **Tecnologias utilizadas:**
- Java 17/21
- Spring Boot
- Spring Web (REST APIs)
- H2 Database
- PostgreSQL com Docker
- PGAdmin
- 
## **Funções:**
- Lista de jogos
- Separação de jogos por categoria de lista
- Reordenação de títulos nas listas
- Endpoints
- 
## **Driagrama:**
![WhatsApp Image 2025-08-21 at 15 38 47](https://github.com/user-attachments/assets/c0dc51ef-b97f-43db-9ecf-162cb7b60502)

## 📁**Estrutura**
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

## 📌**Endpoints**
- ´GET/games
retorna a lista de todos os jogos
| Parâmetro | Tipo |
|---|---|
| id | Long |
