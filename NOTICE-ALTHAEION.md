# NOTICE — version modifiee

Cet outil est une **version modifiee** d'**Element Call**
(https://github.com/element-hq/element-call), redistribuee par Althaeion sous la
GNU Affero General Public License v3.0 (AGPL-3.0) — la meme licence que l'oeuvre
d'origine. Le texte complet est conserve dans `LICENSE-AGPL-3.0`.

## Modifications (AGPL-3.0 §5a)

- La session est ouverte par le serveur local: les pages de connexion et
  d'inscription, ainsi que les entrees « se connecter » / « se deconnecter » du
  menu, ont ete retirees. Ce produit n'a qu'un compte, celui avec lequel la
  personne est deja entree.
- La marque et le logo ont ete remplaces.
- La telemetrie (PostHog, Sentry, rageshake, OpenTelemetry) n'est pas
  configuree, et le repli STUN public est desactive: rien ne quitte la machine.
- Le service de jetons LiveKit (`lk-jwt-service`, publie uniquement en image
  Linux) a ete reecrit pour fonctionner en natif.
- Le serveur Matrix (Synapse) est compile pour Windows, plateforme pour laquelle
  le projet ne publie pas de binaire.

## Source correspondante (AGPL-3.0 §13)

Le code d'origine est disponible chez l'editeur, a l'adresse ci-dessus. Les
modifications listees ci-dessus sont appliquees par les regles de
`runtime/auth-purge.json` et les scripts `runtime/setup-video-calls.mjs`,
`runtime/video-calls-run.mjs` et `runtime/livekit-jwt.mjs`.

LiveKit est distribue sous licence Apache-2.0; son texte est conserve dans
`vendor/livekit/LICENSE`. Synapse est distribue sous AGPL-3.0.
