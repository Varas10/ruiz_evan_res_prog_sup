# Fiche de présentation — Automate Siemens S7-1500 CPU 1511-1 PN

*RUIZ Evan*
## 1. Présentation générale
La **CPU SIMATIC S7-1511-1 PN** (référence **6ES7511-1AK02-0AB0**) est un modèle d'entrée de gamme de la série S7-1500, qui offre un bon compromis entre performance et coût pour des applications d'automatisation de complexité moyenne, avec une communication PROFINET intégrée.

## 2. Caractéristiques techniques principales
| Caractéristique        | Valeur                                                      |
| ---------------------- | ----------------------------------------------------------- |
| Référence              | 6ES7511-1AK02-0AB0                                          |
| Interfaces intégrées   | 1 interface PROFINET (switch 2 ports RJ45)                  |
| Alimentation intégrées | 24V DC                                                      |
| Emplacement mémoire    | Slot pour carte SD                                          |
| Horloge temps réel     | Intégrée, avec sauvegarde                                   |
| Diagnostic             | LED d'état + diagnostic via TIA Portal ou display optionnel |
## 3. Communication PROFINET
La CPU 1511-1 PN intègre **1 interface PROFINET avec un switch de 2 ports RJ45**, permettant :
- Le rôle d'**IO-Controller** (contrôleur PROFINET) pilotant des IO-Devices décentralisés, c'est-à-dire des modules déportés ou des appareils externes. Par exemple :ET 200SP, ET 200MP, variateurs, capteurs communicants...
- Une communication en **temps réel (RT)** 
- Diagnostic à distance des équipements de terrain
- Configuration et programmation via **TIA Portal**

## 4. Protocoles supportés
- **PROFINET IO** (protocole natif principal)
- **S7 Communication** (communication entre CPU Siemens)
- **OPC UA** (serveur intégré selon la version du firmware, pour supervision/IIoT)
- **Modbus TCP** (via bibliothèque logicielle, pas natif matériel)
- **PROFIBUS DP** : non intégré nativement, nécessite un module de communication (CM) additionnel

## 5. Positionnement dans la gamme
La 1511-1 PN est le modèle **d'entrée de gamme** de la série 1500, adapté aux machines simples à moyennement complexes. Pour des besoins plus importants (plus de mémoire, IRT, redondance, sécurité intégrée), Siemens propose les modèles supérieurs (1513, 1515, 1516, 1517, 1518)

---
# Capteur infrarouge PNP — Siemens 3RG6013-3AB00

## 1. Présentation
Le **capteur photoélectrique infrarouge Siemens 3RG6013-3AB00** est un capteur de proximité optique compact, à sortie **PNP**, destiné à la détection de présence et passage d'objets en environnement industriel.

## 2. Principe de fonctionnement
Le capteur émet un faisceau infrarouge et détecte soit sa réflexion sur l'objet cible (NO), soit son interruption (NF). La sortie **PNP** délivre un potentiel **positif (+24V)** sur le fil de sortie lorsque l'état de détection est actif (logique "sourcing").

## 3. Caractéristiques techniques
| Caractéristique               | Valeur                                                        |
| ----------------------------- | ------------------------------------------------------------- |
| Référence                     | 3RG6013-3AB00                                                 |
| Fabricant                     | Siemens                                                       |
| Type                          | Capteur photoélectrique infrarouge, proximité                 |
| Sortie                        | PNP (NO/NF selon câblage)                                     |
| Tension d'alimentation        | 10-30V DC                                                     |
| Portée de détection           | Quelques centimètres à ~1 m (selon variante de la gamme 3RG6) |
| Indice de protection          | IP67                                                          |
| Fréquence de commutation      | jusqu'à 1000 Hz                                               |
| Courant de sortie max         | 200 mA                                                        |
| Température de fonctionnement | -25°C à +60°C                                                 |
## 4. Protocole / intégration industrielle
- **Signal de base** : Tout-Ou-Rien (TOR), câblé directement sur une **entrée numérique (DI)** de l'automate
- **Intégration réseau** : raccordable à une entrée digital de l'automate ou sur un module d'E/S déporté (ex. **ET 200SP**) communiquant en **PROFINET** vers la CPU
- Pas de communication numérique native sur ce modèle (capteur TOR classique, non IO-Link)

---

**Synthèse** : La CPU 1511-1 PN assure la communication PROFINET native en tant qu'IO-Controller pilotant des équipements décentralisés. Le capteur infrarouge PNP Siemens 3RG6013-3AB00 est un organe de détection TOR classique, raccordé sur une entrée digitale de l'automate ou d'un module déporté, lui-même intégré dans l'architecture PROFINET de l'automate.
