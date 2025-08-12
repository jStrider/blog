# Stratégie de protection des branches

## Branches principales

### `main`
- **Rôle** : Branche de production, déploie automatiquement sur GitHub Pages
- **Protection** : 
  - Requiert une Pull Request depuis `develop`
  - Requiert une review avant merge
  - Pas de push direct autorisé

### `develop`
- **Rôle** : Branche de développement, tests et intégration
- **Protection** : 
  - Push direct autorisé pour le développement
  - Tests automatiques sur chaque push

## Workflow de développement

1. **Créer une feature branch** depuis `develop`
   ```bash
   git checkout develop
   git pull origin develop
   git checkout -b feature/nouvel-article
   ```

2. **Développer et commiter**
   ```bash
   # Faire vos modifications
   git add .
   git commit -m "feat: ajout nouvel article"
   ```

3. **Pousser et créer une PR**
   ```bash
   git push -u origin feature/nouvel-article
   # Créer une PR vers develop sur GitHub
   ```

4. **Merge vers develop**
   - Une fois la PR approuvée, merger vers `develop`
   - Les tests s'exécutent automatiquement

5. **Publication**
   - Créer une PR de `develop` vers `main`
   - Une fois approuvée, merger vers `main`
   - Déploiement automatique sur GitHub Pages

## Bonnes pratiques

- Toujours commencer par `develop`
- Utiliser des messages de commit conventionnels
- Tester localement avant de pousser
- Faire des PRs petites et focalisées 