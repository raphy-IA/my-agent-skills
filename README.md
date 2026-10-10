# 🚀 Mon Workspace d'Agents IA

Centralisation et organisation de mes **Skills (consignes)**, **Serveurs MCP (connecteurs)** et **Configurations d'Assistants**.

---

## 📂 Structure du Dépôt

- `1-SKILLS/` : Dossiers de règles métiers, consignes et checklists (`SKILL.md`).
- `2-MCP-SERVERS/` : Connecteurs d'outils et d'API (Bases de données, n8n, GitHub, etc.).
- `3-CONFIGS-ASSISTANTS/` : Fichiers de configuration spécifiques à chaque assistant (Google Antigravity, Claude Desktop, etc.).

---

## 🧠 1. Répertoire des Skills (Instructions & Métier)

| Nom du Skill | Catégorie | Compatibilité | Description / Usage | Source / Lien |
| :--- | :--- | :--- | :--- | :--- |
| **Audit Sécurité Web** | Sécurité | `Universel` | Checklist OWASP, analyse des vulnérabilités JWT/IDOR | `1-SKILLS/Security/` |
| **Revue de Code** | Dev | `Universel` | Analyse de la qualité, lisibilité et refactoring | `1-SKILLS/Code/` |
| **Générateur n8n** | Automation | `Universel` | Consignes pour concevoir des flux JSON n8n valides | `1-SKILLS/Automation/` |
| **Semgrep (Sécurité SAST)** | Sécurité | `Universel` | Analyse statique de failles (Python, Node, etc.) | [github.com/semgrep/semgrep](https://github.com/semgrep/semgrep) |
| **Awesome Agent Skills** | Dev / Qualité | `Universel` | Catalogue de skills de code et bonnes pratiques | [github.com/VoltAgent/awesome-agent-skills](https://github.com/VoltAgent/awesome-agent-skills) |
| **Secure Coding Checklist** | Sécurité | `Universel` | Référentiel de bonnes pratiques de code sécurisé | [github.com/trailofbits/secure-coding-checklist](https://github.com/trailofbits/secure-coding-checklist) |

---

## 🔌 2. Serveurs MCP (Connecteurs & Outils)

| Nom du Serveur MCP | Service Connecté | Compatibilité | Rôle principal | Dépôt Source GitHub |
| :--- | :--- | :--- | :--- | :--- |
| **n8n MCP** | n8n | `Antigravity` / `Claude` | Interaction directe avec les workflows n8n | [Lien GitHub](https://github.com/...) |
| **Filesystem MCP** | Fichiers locaux | `Antigravity` / `Claude` | Lecture/Écriture et édition de fichiers dans vos projets | [github.com/modelcontextprotocol/servers](https://github.com/modelcontextprotocol/servers) |
| **PostgreSQL MCP** | Base PostgreSQL | `Antigravity` / `Claude` | Inspection du schéma BDD et exécution de requêtes SQL | [github.com/modelcontextprotocol/servers](https://github.com/modelcontextprotocol/servers) |
| **GitHub MCP** | API GitHub | `Antigravity` / `Claude` | Interaction avec vos dépôts, PR, et issues à distance | [github.com/modelcontextprotocol/servers](https://github.com/modelcontextprotocol/servers) |
| **Git MCP** | Git Local | `Antigravity` / `Claude` | Analyse des diffs de code et de l'historique des commits | [github.com/modelcontextprotocol/servers](https://github.com/modelcontextprotocol/servers) |

---

## ⚙️ 3. Configurations des Assistants

- 🟢 **Google Antigravity :** Configurations d'agents et chemins d'accès (`3-CONFIGS-ASSISTANTS/antigravity/`).
- 🟠 **Claude Desktop :** Fichier `claude_desktop_config.json` (`3-CONFIGS-ASSISTANTS/claude/`).
- {
  "mcpServers": {
    "filesystem": {
      "command": "npx",
      "args": [
        "-y",
        "@modelcontextprotocol/server-filesystem",
        "/chemin/vers/vos/projets/code"
      ]
    },
    "postgresql": {
      "command": "npx",
      "args": [
        "-y",
        "@modelcontextprotocol/server-postgres",
        "postgresql://utilisateur:motdepasse@localhost:5432/mabase"
      ]
    }
  }
}

---

## 📌 Guide d'Ajout Rapide

1. **Un nouveau Skill ?** Créez un sous-dossier dans `1-SKILLS/` avec un fichier `SKILL.md` et ajoutez une ligne au tableau 1.
2. **Un nouveau Serveur MCP ?** Référencez son dépôt GitHub source dans le tableau 2 et ajoutez sa configuration dans `3-CONFIGS-ASSISTANTS/`.
