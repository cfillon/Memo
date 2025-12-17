
# 01 — Prise en main & installation

## Prérequis
- Accès **GitHub** au dépôt.
- **Git** 2.40+.
- **PowerShell 7+** (Core) recommandé.
- **SSH** et/ou **GitHub CLI (`gh`)**.

### Installer PowerShell 7
- Windows : Microsoft Store ou package MSI (docs Microsoft)
- Linux : via packages Microsoft (apt/yum)

Vérifier :
```powershell
$PSVersionTable.PSVersion
```

### Git + identité
```powershell
git config --global user.name "Prénom Nom"
git config --global user.email "prenom.nom@exemple.com"
```

### Authentification SSH
```powershell
ssh-keygen -t ed25519 -C "prenom.nom@exemple.com"
# Ajouter ~/.ssh/id_ed25519.pub dans GitHub > Settings > SSH and GPG keys
ssh -T git@github.com
```

### Cloner `New_Repo`
```powershell
git clone git@github.com:ORGANISATION/New_Repo.git
cd New_Repo
```

### GitHub CLI (utile pour PR/Review)
```powershell
winget install GitHub.cli  # Windows
# ou voir https://cli.github.com/ pour autres OS
gh auth login
```
