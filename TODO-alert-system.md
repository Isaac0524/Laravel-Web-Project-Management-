# Système d'Alerte - Plan d'Implémentation

## Objectif
Implémenter un système d'alerte avec bip sonore pour :
- ✅ Alertes vertes : début d'un projet (start_date = aujourd'hui)
- ✅ Alertes rouges : retards (1 semaine avant l'échéance)

## Étapes à compléter

### Phase 1: Backend (DashboardController)
- [ ] Modifier DashboardController pour calculer les alertes
- [ ] Ajouter la logique de détection des projets qui commencent aujourd'hui
- [ ] Ajouter la logique de détection des projets en retard (1 semaine avant)
- [ ] Passer les données d'alerte aux vues

### Phase 2: Système JavaScript d'alertes
- [ ] Créer `resources/js/alerts.js`
- [ ] Implémenter les fonctions de notification toast
- [ ] Ajouter la fonctionnalité de son (bip)
- [ ] Gérer les types d'alertes (vert/rouge)

### Phase 3: Styles CSS
- [ ] Créer `resources/css/alerts.css`
- [ ] Styles pour alertes toast
- [ ] Styles pour indicateurs visuels dans les projets
- [ ] Couleurs vertes et rouges

### Phase 4: Modifications des vues
- [ ] Modifier `dashboard.blade.php` pour afficher les alertes
- [ ] Modifier `projects/index.blade.php` pour les indicateurs
- [ ] Modifier `layout.blade.php` pour inclure JS/CSS

### Phase 5: Intégration audio
- [ ] Créer le dossier `public/sounds/`
- [ ] Ajouter les fichiers audio pour les bips
- [ ] Intégrer la lecture audio

### Phase 6: Configuration Vite
- [ ] Modifier `vite.config.js` pour inclure le nouveau JS

## Fichiers à créer/modifier
- [ ] `pm-app/app/Http/Controllers/DashboardController.php` (modification)
- [ ] `pm-app/resources/js/alerts.js` (nouveau)
- [ ] `pm-app/resources/css/alerts.css` (nouveau)
- [ ] `pm-app/resources/views/dashboard.blade.php` (modification)
- [ ] `pm-app/resources/views/projects/index.blade.php` (modification)
- [ ] `pm-app/resources/views/layout.blade.php` (modification)
- [ ] `pm-app/vite.config.js` (modification)
- [ ] Fichiers audio dans `pm-app/public/sounds/`

## Tests à effectuer
- [ ] Alertes visuelles fonctionnelles
- [ ] Sons joués correctement
- [ ] Performance sur différentes vues
- [ ] Alertes seulement pour les gestionnaires

## Notes
- Utiliser des sons discrets mais perceptibles
- Design moderne et cohérent avec l'interface existante
- Gérer les permissions (uniquement pour les managers)
