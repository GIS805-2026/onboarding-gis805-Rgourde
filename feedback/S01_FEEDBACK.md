# Rétroaction automatisée -- S01 (Diagnostic fondamental -- NexaMart kickoff)

_Générée le 2026-05-15T12:52:31+00:00 -- Run `20260515T125138Z-ff34aff5`_

Ce document est produit par un pipeline reproductible (vérification SQL déterministe + analyse LLM du brief et de la déclaration IA). Une revue humaine précède toujours sa publication. **À ce stade expérimental, aucune note ni étiquette de niveau n'est diffusée : l'objectif est purement formatif.**

> ⚠️ **Avertissement instructeur (à retirer avant publication) :** cette analyse a été générée avec `--skip-pull`. Le contenu correspond au commit local et **n'est peut-être pas la dernière version poussée par l'étudiant·e**.

---

## 1. Vérification automatique de la requête SQL

La requête extraite de votre brief n'a pas pu être validée automatiquement. Quelques pistes constructives ci-dessous pour vous aider à la rendre exécutable et alignee avec la question posée.

_Observation technique : aucune requête SQL détectée dans le brief_


**Pistes :**
> Aucun bloc ```sql ... ``` détecté et l'extracteur LLM n'a trouvé aucune requête. Encadrez votre requête finale dans la section « Preuve » avec un bloc ```sql ... ``` pour fiabiliser l'auto-validation.
> Extracteur LLM : Le brief fourni ne contient aucune requête SQL à extraire.

## 2. Rétroaction pédagogique sur le brief

> Le brief soumis est essentiellement vide : les sections clés (réponse exécutive, modèles, preuves et validations) ne contiennent pas d'information exploitable. Remplissez d'abord le grain et la réponse exécutive, puis ajoutez une requête de validation et un README pour la reproductibilité.

### Observations par dimension

**Model quality**
- Observation : Le brief ne contient aucun énoncé de grain, ni de schéma dimensionnel — sections vides.
- Piste d'amélioration : Indiquer immédiatement le grain (ex. ligne de commande) et lister les dimensions et mesures clés (product, date, store, customer, channel).

**Validation quality**
- Observation : Aucune requête SQL de validation fournie dans la section « Preuve ».
- Piste d'amélioration : Fournir au moins une requête de validation (GROUP BY) qui calcule le revenu net par catégorie/région/trimestre et décrire les checks (NULLs, doublons).

**Executive justification**
- Observation : La section « Réponse exécutive » est vide et n'adresse pas la question du CEO.
- Piste d'amélioration : Écrire un résumé décisionnel de 150–300 mots répondant à la question CEO et incluant une recommandation claire (p.ex. valider le schéma étoile v1).

**Process trace**
- Observation : Aucune trace de commits, ni note sur l'usage d'IA ou le decision log dans le brief.
- Piste d'amélioration : Ajouter l'historique Git (≥1 commit au minimum) et une note IA indiquant outils + validation humaine, puis décrire les décisions de modélisation prises.

**Reproducibility**
- Observation : Aucune instruction de reproduction ni READMEs/chemins documentés — sections vides.
- Piste d'amélioration : Inclure un README minimal expliquant comment cloner, exécuter le script de checks (DuckDB/make) et obtenir les mêmes résultats.

_Quelques points appellent une attention particulière lors de la prochaine itération : sections_vides._

## 3. Déclaration d'utilisation de l'IA

> Le fichier fournit un bon gabarit et un exemple montrant l'étape et une validation humaine. Il manque toutefois des informations obligatoires (version/modèle précis et mentions des limites/erreurs), et le gabarit semble encore non rempli pour votre remise.

**Sujets bien couverts dans votre déclaration :**

- à quelle étape l'IA a été utilisée
- comment la sortie a été validée par l'humain

**Sujets à ajouter ou expliciter pour la prochaine itération :**

- outils utilisés (nom + version/modèle)
- limites ou erreurs observées

## 4. Pistes d'action pour la prochaine itération

- Reprendre la requête de la section « Preuve » pour qu'elle s'exécute sur `db/nexamart.duckdb` et qu'elle produise la forme attendue (voir pistes en section 1).
- Réviser le brief en tenant compte des observations par dimension de la section 2.
- Compléter `ai-usage.md` en y ajoutant : outils utilisés (nom + version/modèle).
- Compléter `ai-usage.md` en y ajoutant : limites ou erreurs observées.

---

## 5. Traçabilité

- **Run ID :** `20260515T125138Z-ff34aff5`
- **Devoir :** `S01`
- **Étudiant·e :** `Rgourde`
- **Commit analysé :** `887e435`
- **Audit (côté instructeur) :** `tools/instructor/feedback_pipeline/audit/20260515T125138Z-ff34aff5/Rgourde/`
- **Prompts (SHA-256) :**
  - `sql_extractor_system` : `90ee9e277de7a27f...`
  - `rubric_grader_system` : `505f32d1d8319d66...`
  - `ai_usage_grader_system` : `81cb7fdf89bda55a...`
- **Fournisseur (rubrique) :** `openai`
- **Fournisseur (IA-usage) :** `openai` (gpt-5-mini-2025-08-07)

_Ce feedback a été produit par un pipeline automatisé et **revu par l'équipe pédagogique avant publication**. Aucun chiffre ni étiquette de niveau n'est diffusé à ce stade expérimental : l'objectif est uniquement formatif. Ouvrez une issue dans ce dépôt pour toute question._
