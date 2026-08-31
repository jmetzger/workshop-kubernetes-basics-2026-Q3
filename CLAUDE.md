# CLAUDE.md - workshop-kubernetes-basics-2026-Q3

## Was ist das hier

Trainings-Repo "Kubernetes - Modul Basics" (2 Trainingstage) fuer ein
Inhouse-Training im September 2026. Schwester-Repo: `workshop-kubernetes-advanced-2026-Q3`
(Modul Advanced). Dieses Repo ist PUBLIC und enthaelt bewusst keinen Kundenbezug -
auch in Commits, Dateien und Issues keinen Kundennamen nennen.

Vollstaendige Kopie von `training-kubernetes-einfuehrung` (Stand 31.08.2026),
nur der README-Titel wurde angepasst. Die README.md ist die Agenda; sie enthaelt
noch die komplette Einfuehrungs-Agenda und kann fuer die 2,5 Basics-Tage
(Container & Cloud-native, Kubernetes-Einstieg/Architektur/kubectl,
Pods/Deployments/StatefulSets/Jobs, Storage & ConfigMaps/Secrets,
Netzwerke/Services/Ingress, Helm, Troubleshooting) noch gestrafft werden.

Aenderungen an Uebungen bitte HIER machen, nicht im Quell-Repo -
dieses Repo ist die fuer das Training massgebliche Kopie.

## Trainingsumgebung

- GETEILTER Trainingscluster fuer alle Teilnehmer (DOKS + Bastion-Client).
- Namespace-Strategie daher: `<prefix>-<dein-name>` (z.B. `resource-<dein-name>`),
  Namespace beim `kubectl apply -n ...` angeben, nicht im Manifest.
- Zugang per Putty/SSH oder Chrome (Guacamole) auf Bastion-Client.

## Konventionen (Kurzfassung Skill workshop-training)

- Keine Umlaute in neuen Dateien (ae/oe/ue/ss), Dateiendung `.yml`, Manifests nummerieren.
- Code-Bloecke ohne Sprach-Annotation.
- Neue Uebungen MUESSEN auf einem echten Cluster getestet werden, bevor sie in die Agenda kommen.
- Jede neue Uebung in der README-Agenda verlinken.
- PDF: `gh workflow run pdf-deployment.yml --repo jmetzger/github-md2pdf --field repository=workshop-kubernetes-basics-2026-Q3`
