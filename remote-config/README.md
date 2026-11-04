# Remote Config

Schalter, die Apps beim Start lesen — ohne App-Update. Geschrieben vom RevCockpit (Tab „Remote-Config“) oder per Terminal. Nur der Repo-Eigentümer kann sie ändern; lesen muss sie jeder können, weil die App ohne Anmeldung abruft. Sie enthalten keine Preise, Schlüssel oder Nutzerdaten.

| Datei | App | Schlüssel | Werte |
|---|---|---|---|
| `dayplan.json` | DayPlan | `paywallOffer` | `standard` · `lifetimeFocus` |
| `padeltracker.json` | Padel Score Tracker | `paywallOffer` | `standard` · `lifetimeFocus` |
| `runarc.json` | RunArc | `paywallOffer` | `standard` · `lifetimeFocus` |
| `stretchzen.json` | StretchZen | `paywallOffer` | `standard` · `lifetimeFocus` |
| `spendra-android.json` | Spendra (Android) | `paywallOffer` | `standard` · `lifetimeFocus` |
| `spendra.json` | Budget & Bill Planner: Spendra (iOS, ab 1.3.0) | `paywallOffer` | `standard` · `lifetimeFocus` |
| `tyempo.json` | Tyempo (iOS, ab 1.3.0) | `paywallOffer`, `paywallProducts` | `standard` · `yearlyFocus`; Produkt-Tausch `{"tyempo_premium_1m": "tyempo_premium_1m_199"}` |

## `paywallProducts` — Preisstufen tauschen

Optional, ab Apps mit Preistausch (Tyempo 1.3.0): `{ "<Standard-Produkt-ID>": "<Ersatz-Produkt-ID>" }`.
Die App zeigt im Tarif statt des Standard-Produkts das Ersatzprodukt — Aufbau und Texte der Paywall
bleiben gleich. Kann sie es nicht laden, nimmt sie das Standard-Produkt. Fehlt der Schlüssel, wird nichts getauscht.
