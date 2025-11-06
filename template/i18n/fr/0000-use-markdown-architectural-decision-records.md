# 0000 - Utiliser MADR (Markdown Architectural Decision Records)


## Contexte et énoncé du problème

Nous souhaitons consigner les décisions architecturales prises dans le cadre de ce projet, qu'elles concernent l'architecture (« fiche de décision architecturale »), le code ou d'autres domaines. Quel format et quelle structure ces fiches doivent-elles respecter ?

## Options considérées

- [MADR 4.0.0](https://adr.github.io/madr/) – The Markdown Architectural Decision Records
- [Michael Nygard's template](http://thinkrelevance.com/blog/2011/11/15/documenting-architecture-decisions) - The first incarnation of the term "ADR"
- [Sustainable Architectural Decisions](https://www.infoq.com/articles/sustainable-architectural-design-decisions) - The Y-Statements
- Other templates listed at https://github.com/joelparkerhenderson/architecture_decision_record
- Formless – No conventions for file format and structure

## Résultat de la décision

Option choisie = "MADR 4.0.0", parce que

* Les hypothèses implicites doivent être explicitées. La documentation de conception est importante pour permettre aux gens de comprendre les décisions prises ultérieurement. Voir aussi ["A rational design process: How and why to fake it"](https://doi.org/10.1109/TSE.1986.6312940).
* MADR permet de consigner de manière structurée toute décision.
* Le format MADR est concis et correspond à notre style de développement.
* La structure MADR est compréhensible et facilite l'utilisation et la maintenance.
* Le projet MADR est très vivant.

### Conséquences

Les nouvelles décisions seront maintenant à tracer dans une fiche.

Sont potentiellement exemptées les décisions temporaires/à durée de vie limitée, les décisions à portée limitée (coût faible/risque faible) ou les décisions qui sont déjà couvertes ailleurs.
