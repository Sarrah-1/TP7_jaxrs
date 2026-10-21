# TP 7 : API REST avec JAX-RS (Jersey) et Spring Boot

Application de gestion de comptes bancaires exposant une API REST CRUD,
au format **JSON** et **XML**, avec une base de données H2 en mémoire.

## Structure du projet

```
src/main/java/ma/ws/jaxrs
├── JaxrsApplication.java          # Classe principale + CommandLineRunner
├── config/MyConfig.java           # Enregistrement de Jersey (ResourceConfig)
├── entities/
│   ├── Compte.java                # Entité JPA (+ @XmlRootElement)
│   └── TypeCompte.java            # Enum COURANT / EPARGNE
├── repositories/
│   └── CompteRepository.java      # JpaRepository<Compte, Long>
└── web/
    └── CompteRestJaxRSAPI.java    # Endpoints REST JAX-RS
```

## Endpoints

| Méthode | URL                        | Description                 |
|---------|----------------------------|-----------------------------|
| GET     | `/banque/comptes`          | Liste de tous les comptes   |
| GET     | `/banque/comptes/{id}`     | Un compte par identifiant   |
| POST    | `/banque/comptes`          | Créer un compte             |
| PUT     | `/banque/comptes/{id}`     | Modifier un compte          |
| DELETE  | `/banque/comptes/{id}`     | Supprimer un compte         |

##Screen

<img width="622" height="121" alt="TP7_1" src="https://github.com/user-attachments/assets/7541cfc2-ea1d-429b-b174-cd35498a2d26" />

<img width="729" height="301" alt="TP7_2" src="https://github.com/user-attachments/assets/a8488f3c-d2da-4ca1-9ab3-788a98709f81" />

<img width="462" height="286" alt="TP7_3" src="https://github.com/user-attachments/assets/aff90070-3db1-4bb2-809b-c42df1d75699" />
