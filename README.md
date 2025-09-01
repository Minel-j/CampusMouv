# 📌 Campus Mouv

## 🚀 Présentation du projet

La société **ENI** souhaite développer pour ses stagiaires actifs ainsi que ses anciens stagiaires une **plateforme web privée** leur permettant d’organiser des sorties.  
L’inscription est gérée par un ou plusieurs administrateurs.  
Les sorties ainsi que les participants sont rattachés à un campus afin de permettre une organisation **géographique** des événements.

### 🎯 Constat
- Le grand nombre de stagiaires répartis sur différents campus ne permet pas une organisation simple.  
- Il n’existe pas de **canal officiel** pour proposer ou consulter les sorties.  
- Les outils actuels ne gèrent pas :
  - Les invitations selon la localisation ou les intérêts.  
  - Le nombre de participants.  
  - Les dates limites d’inscription.  

👉 Une solution réussie doit permettre d’**organiser facilement** les sorties et d’anticiper le nombre de participants, le lieu et les informations nécessaires.

---

## ⚙️ Pré-requis

- **PHP** >= 8.3  
- **Symfony** >= 6.4  
- **Symfony CLI** >= 5.12.0  
- **Composer** >= 2.8.1  
- **Twig** >= 3.21.1  
- **Doctrine/ORM** >= 3.5.2  
- **MySQL** >= 8.0  

---

## 📥 Installation & lancement

1. **Installer les dépendances**
   ```bash
   composer install
   ```

2. **Configurer la base de données**  
   Dans votre fichier `.env.local` :
   ```dotenv
   DATABASE_URL="mysql://root:@127.0.0.1:3306/campusmouv?serverVersion=8.0.32&charset=utf8mb4"
   ```

3. **Configurer Cloudinary** (gestion des photos de profil et de sorties)  
   ```dotenv
   ###> cloudinary ###
   CLOUDINARY_CLOUD_NAME=ton_cloud_name
   CLOUDINARY_API_KEY=ton_api_key
   CLOUDINARY_API_SECRET=ton_api_secret
   ```

4. **Configurer Papercut** (gestion des mails : mot de passe oublié, désinscription)  
   - Télécharger [Papercut SMTP](https://github.com/ChangemakerStudios/Papercut-SMTP/releases)  
   - Écouter sur le port **25**  

5. **Exécuter les commandes suivantes :**
   ```bash
   composer install
   symfony console doctrine:database:create
   symfony console doctrine:migrations:migrate
   symfony console doctrine:fixtures:load
   symfony serve
   ```

---

## ❗ Problématiques rencontrées

- 📧 Gestion des mails : fonctionnement en local via Papercut pas encore optimal → nécessite des ajustements.  

---

## 👥 Comptes de test

### 🔑 Admin (dev)
- **Nom :** DUDU  
- **Prénom :** Florent  
- **Email :** florent.dudu@campus-eni.fr  
- **Mot de passe :** `F.dudu2025`  
- **Campus :** Rennes  

### 🔑 Utilisateur simple
- **Nom :** PAPA  
- **Prénom :** Alex  
- **Email :** alex.papa@campus-eni.fr  
- **Mot de passe :** `A.papa2025`  
- **Campus :** Rennes  

---

## 🛠️ Équipe & Contact

En cas de bug, merci de contacter :

- [Jonathan MINEL](https://github.com/Minel-j)  
- [Laurine SUSS](https://github.com/laurine-s)  
- [Laurence GUILLEVIC](https://github.com/LaurenceGlc)  
- [Romane BOULIER](https://github.com/rfboulier)  
