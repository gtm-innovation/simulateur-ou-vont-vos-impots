# Simulateur : où vont vraiment vos impôts ?

Calculateur web qui montre, à partir du salaire net mensuel d'un utilisateur, ce qu'il reverse chaque année à l'État et à la Sécu (IR + cotisations salariales + TVA estimée), et où va chaque euro selon la répartition du budget public 2026.

**Live** : https://moneyradar.org/simulateur-ou-vont-vos-impots/

## Aperçu

- Calcul de l'IR avec le barème officiel 2026 (revenus 2025) + décote Art. 197-I-4 CGI
- Cotisations salariales selon les taux URSSAF 2026 (salarié non-cadre / cadre / indépendant / retraité)
- TVA estimée par décile de revenu disponible (INSEE Analyses 43)
- Répartition selon le budget public 2026 (1 722 Md€) : retraites, santé, éducation, charge de la dette, etc.
- Tableau ligne par ligne du détail (jusqu'au coût de l'Élysée, de l'Assemblée et du Sénat)
- Comparaison Europe : taux de prélèvements obligatoires (Eurostat / OCDE 2024)

## Intégration

Le fichier `index.html` est autonome : un seul fichier qui contient le HTML, le CSS et le JS. Aucune dépendance externe (sauf l'iframe Beehiiv pour le lead magnet et le logo MoneyRadar hébergé chez le client).

Pour l'embed WordPress, coller le contenu de `index.html` dans un bloc HTML personnalisé.

## Sources des données

- **Barème IR 2026** : [service-public.gouv.fr](https://www.service-public.gouv.fr/particuliers/vosdroits/F1419)
- **Décote** : Art. 197-I-4 du Code général des impôts (constantes 897 € / 1 483 €, seuils 1 982 € / 3 277 €)
- **Cotisations sociales** : [URSSAF 2026](https://www.urssaf.fr/accueil/outils-documentation/taux-baremes/taux-cotisations-secteur-prive.html)
- **Budget public 2026** : [LFI 2026 + LFSS 2026](https://www.budget.gouv.fr/reperes/loi-finances/dossiers/plf_2026)
- **TVA par décile** : [INSEE Analyses n° 43](https://www.insee.fr/fr/statistiques/3713290)
- **Taux PO Europe** : Eurostat / OCDE 2024

## Précision

Le calcul est précis à environ ± 5 % près. Pour un calcul à l'euro près, utiliser le [simulateur officiel impots.gouv.fr](https://simulateur-ir-ifi.impots.gouv.fr/calcul_impot/2026/complet/index.htm).

## Périmètre

Le calculateur inclut **uniquement les prélèvements visibles** :
- IR retenu à la source
- Cotisations salariales (~22 % du brut)
- TVA estimée sur consommation

Il **exclut** les cotisations patronales (~42 % du brut, payées par l'employeur en plus du salaire et qui ne transitent pas par les poches du contribuable). Une mention en évidence rappelle leur existence pour situer le "coin fiscal" OCDE complet.

## Licence

© MoneyRadar.
