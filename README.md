# 🔔 Push Notif – Backend (Spring Boot)

Ce dépôt contient la partie **backend** du projet Push Notif, développé avec **Spring Boot**.  
Il fournit une API REST sécurisée pour envoyer des notifications via **email**, **SMS (Twilio)** et potentiellement des notifications push.

---

## ✨ Fonctionnalités principales

- 📧 Envoi d'emails via SMTP (JavaMail)
- 📱 Envoi de SMS via Twilio API
- 🔐 Variables sensibles stockées dans un fichier `.env` ou dans les `application.properties`
- 🛠️ Intégration possible avec Firebase Cloud Messaging (FCM) pour les notifications push
- 🗂️ Architecture MVC propre avec Spring Boot
- 🌐 API REST compatible avec un frontend Angular/React

---

## 🛠️ Technologies utilisées

| Composant            | Technologie                  |
|----------------------|------------------------------|
| Langage              | Java 17+                     |
| Framework            | Spring Boot 3+               |
| Build tool           | Maven                        |
| Email                | JavaMailSender (Spring Mail) |
| SMS                  | Twilio API                   |
| Sécurité & config    | Spring Boot Config + .env    |
| Test                 | JUnit / MockMVC              |

---

## 🚀 Lancer le projet localement

### 1. Cloner le repo

```bash
git clone https://github.com/mhbelkahla2001/PushNotif.git
cd backend
```

### 2. Configurer les variables sensibles

Crée un fichier `application.properties` dans `src/main/resources` ou utilise un `.env`, avec :

```properties
# SMTP
spring.mail.host=smtp.gmail.com
spring.mail.port=587
spring.mail.username=your_email@gmail.com
spring.mail.password=your_password
spring.mail.properties.mail.smtp.auth=true
spring.mail.properties.mail.smtp.starttls.enable=true

# Twilio
twilio.account.sid=ACxxxxxxxxxxxxxxxxxxxx
twilio.auth.token=xxxxxxxxxxxxxxxxxxxx
twilio.phone.number=+216xxxxxxxx

# Autres
server.port=8080
```

> 🔐 Ne jamais versionner ce fichier : ajoute-le dans `.gitignore`

---

### 3. Lancer le projet

```bash
./mvnw spring-boot:run
```
ou
```bash
mvn spring-boot:run
```

---

## 📦 Structure du projet

```
backend/
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   └── com/pushnotif/
│   │   │       ├── controller/
│   │   │       ├── service/
│   │   │       ├── model/
│   │   │       └── PushNotifApplication.java
│   │   └── resources/
│   │       ├── application.properties
│   │       └── templates/
├── pom.xml
└── README.md
```

---

## 🧪 Tester l'API

Tu peux tester les endpoints avec **Postman** ou **cURL** :

- `POST /api/notify/email`
- `POST /api/notify/sms`

---

## 👨‍💻 Auteur

- **Nom** : Benkahla Mohamed El Habib  
- 🎓 Projet stage d'été – Proxym-IT Sousse 


---

## 📜 Licence

Projet à but pédagogique. Pour tout usage professionnel, merci de contacter l'auteur.
