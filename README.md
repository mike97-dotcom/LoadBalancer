# 🚀 LoadBalancer en Rust

Bienvenue dans ce projet de **Load Balancer** développé en Rust 🦀 !  
Ce projet utilise l'algorithme de **Round Robin** pour distribuer intelligemment les requêtes entrantes vers plusieurs serveurs. C'est une implémentation simple et efficace pour apprendre les bases des équilibreurs de charge.  

---

## ✨ Fonctionnalités

- ⚙️ **Distribution efficace** : Les requêtes entrantes sont équilibrées entre plusieurs serveurs grâce à l'algorithme de *Round Robin*.
- 🛠️ **Configuration dynamique** : Ajoutez ou modifiez les adresses des serveurs directement via la ligne de commande.
- 📜 **Journaux détaillés** : Suivi précis des événements et outils de débogage pour simplifier le déploiement et le dépannage.

---

## 📋 Prérequis

Assurez-vous que votre environnement respecte les conditions suivantes :

1. 🦀 Installer **Rust** depuis la [page officielle](https://www.rust-lang.org/).
2. ⚒️ Installer les **outils de développement C++** de Visual Studio.
3. 🐍 Avoir **Python 3.x** d'installé sur votre machine.
4. 📦 Installer les bibliothèques Python nécessaires : `Flask`.

### 🛠️ Installation des dépendances Python

Pour installer la dépendance Python nécessaire, exécutez la commande suivante (dans un terminal) :

```bash
pip install Flask
```
🚀 **Utilisation**


1️⃣ Lancez les serveurs Python
Commencez par démarrer vos serveurs Flask en utilisant les commandes suivantes :
```bash
python3 server1.py
python3 server2.py
```
💡 Assurez-vous de vérifier et de modifier les adresses IP des serveurs si nécessaire avant de les lancer.



2️⃣ Configurer et lancer le LoadBalancer
Ajoutez les adresses IP de vos serveurs directement dans le code du Load Balancer. Voici un exemple de configuration statique :
```bash
let lb = LoadBalancer::new(
    "Votre_IP:8080",
    vec!["IP_Serveur1:8000", "IP_Serveur2:8001"].iter().map(|s| s.to_string()).collect()
);
```
3️⃣ Effectuer les tests 🧪
Pour tester que tout fonctionne correctement, vous pouvez exécuter la commande suivante dans votre terminal :
```bash
cargo test
```
4️⃣ Démarrez le LoadBalancer 🚀
Pour exécuter le Load Balancer, utilisez cette commande :
```bash
cargo run
```
Si vous souhaitez personnaliser les adresses IP du serveur d'écoute et des serveurs secondaires, exécutez :
```bash
cargo run -- -b 192.168.1.137:8080 -s IP_Serveur1:8000,IP_Serveur2:8001
```
5️⃣ Accéder via le navigateur 🌐
Ouvrez votre navigateur web et saisissez l'adresse suivante :
```bash
http://Votre_IP:8080
```
