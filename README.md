[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/b5MRUqco)

Installation
1️⃣ Installer Rust
rustc --version
cargo --version

Si non installé :
 https://www.rust-lang.org/tools/install

2️⃣ Ajouter les dépendances

Dans Cargo.toml :

[dependencies]
sysinfo = "0.30"
chrono = "0.4"
prettytable = "0.10"
▶️ Exécution du projet
🖥️ 1. Lancer le serveur

Dans le dossier du projet :

cargo run
✔️ Résultat attendu :
Server running on port 7878
💻 2. Connexion client

Depuis un autre terminal ou PC :

telnet 127.0.0.1 7878

ou

nc 127.0.0.1 7878
⌨️ Commandes disponibles

Une fois connecté, vous pouvez taper :

Commande	Description
cpu	Affiche l’utilisation CPU
mem	Affiche la mémoire utilisée
ps	Liste des processus
all	Vue complète système
help	Liste des commandes
quit	Quitter la connexion
📊 Exemple de rendu
🔹 CPU
CPU Usage: 23.45%
>
🔹 MEM
Memory: 2048/8192 MB
>
🔹 PS
1234     chrome.exe           12.30%
5678     code.exe              8.10%
8901     explorer.exe          2.50%
>
🔹 ALL (tableau complet)
+-------+------------+---------+
| PID   | NAME       | CPU (%) |
+-------+------------+---------+
| 1234  | chrome.exe | 12.30   |
| 5678  | code.exe   | 8.10    |
+-------+------------+---------+

CPU : 23.45%
MEM : 4096/8192 MB
>
📝 Logs système

Toutes les commandes sont enregistrées automatiquement dans :

syswatch.log
Exemple :
[2026-04-22 14:05:12] Command: cpu
[2026-04-22 14:05:15] Command: mem
[2026-04-22 14:05:18] Command: ps
[2026-04-22 14:05:25] Command: all
[2026-04-22 14:05:30] Command: quit
            