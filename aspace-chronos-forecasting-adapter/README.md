# A'Space adapter — chronos-forecasting

**Adresse :** `fiber:a0:chronos-forecasting` — D-N053 pas A (design Clara, dispatch D-N053).
**Fork souverain :** `Amdkn/chronos-forecasting` (parent `amazon-science/chronos-forecasting`, branche `main`).
**Gel amont :** `1224fafa91e1ecd6674f5204066b159e40b5e4a1` (« Compute series lengths in row order so predict_df handles categorical item ids (#537) »).
**Bind Cordis Fiber (16L) :** `e049fe2e20c0552324b3a1003d55c4e5b3a1b28f` — `aspace-plugin.json`, re-applique VERBATIM sur `main` au-dessus de l'adapter (F8 D2).
**Licence :** `Apache-2.0`.
**Version adapter :** 0.1.0 — contrat seul, patron D-N048 (dify / cordis).

## Ce que fait l'adapter

Chronos : prevision de series temporelles pre-entrainee (Chronos, Chronos-2, Chronos-Bolt). Poids : telechargement explicite par l'utilisateur via from_pretrained, jamais monte dans le fork.

Surface : `validate()` (constate : gel, licence, importabilite amont, poids
presents dans le fork, zero appel reseau), `doctor()` (liste de controles),
`describe()` (manifeste machine). **Aucun fichier amont touche, aucun appel
reseau, aucun poids monte dans le fork.**

## Confinement

Aucun confinement commercial : code Apache-2.0, poids Chronos distribues sous Apache-2.0 par l'amont. Usage B2B autorise par la licence.

## Tests

```bash
python -m pytest aspace-chronos-forecasting-adapter/tests/test_smoke.py -v
```

Smoke : constantes (gel 40-hex, adresse fiber, licence), `validate()` vert,
`doctor()` tout ok, import amont, zero import reseau dans l'adapter.
La suite amont est celle du module au gel (voir la fiche d'adaptation :
`chronos-forecasting-ADAPTATION.md`, evidence D-N053/a/chronos-forecasting/).
