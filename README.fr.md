# security.bobine.fit

English version: [README.md](README.md).

Site statique de divulgation de vulnérabilités de [Bobine](https://github.com/FantasmaGlad/Bobine), servi par GitHub Pages sur <https://security.bobine.fit>.

Il publie la clé OpenPGP de réception des rapports, son empreinte, une copie du `security.txt` signé et un renvoi vers la politique complète. Il constitue un canal de vérification de l'empreinte indépendant du site principal `bobine.fit`.

| Fichier | Rôle |
|---|---|
| `index.html`, `fr/index.html` | page d'accueil en anglais et en français |
| `snake/index.html` | jeu Snake |
| `security.asc` | clé publique OpenPGP (empreinte `23CA D324 C507 FB0F 97E6 AECA 6E4C 020E F8BD FEB2`) |
| `.well-known/security.txt` | copie du fichier signé (RFC 9116), identique à celle de `bobine.fit` |
| `CNAME`, `.nojekyll` | domaine personnalisé ; `.nojekyll` est indispensable pour servir `.well-known` |
| `robots.txt`, `sitemap.xml`, `llms.txt` | indexation |

## Maintenance

La clé, son empreinte et `security.txt` doivent rester identiques à ceux de `bobine.fit` et du dépôt Bobine (`docs/security/`). Lors d'un renouvellement ou d'une rotation de clé, mettre à jour ce dépôt dans la même opération et vérifier que l'empreinte est la même sur tous les canaux.

Une surveillance quotidienne vérifie que le domaine résout toujours vers ce dépôt et que l'empreinte servie est la bonne.

## Licence

AGPL-3.0, voir [LICENSE](LICENSE).
