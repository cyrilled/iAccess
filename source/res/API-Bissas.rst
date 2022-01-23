Annexe - Description des API des drivers de bissas
==================================================

:Date: 02-24 8h-11h
:Type: Réunion
:Lieu: Neuilly - EHPAD Rives de Seine de Ryokan
:PartiesPrenantes: ABI, JDR, PSO, AGO
:Organisateur: ABI
:Rapporteur: KWG
:Presents: ABI, JDR, PSO, AGO, EDT
:Objectifs: Cas d'étude EHPADs de Ryokan

.. attention::
    Ce compte rendu est un *document de travail* et n'est pas contractuel.

Nouvel intervenant, directeur de l'EHPAD Rives de Seine à Neuilly :
 - Etienne Dumont (EDT) - Neuilly, Ryokan

#. Quel que soit le type de badge, les informations envoyées par le driver du bissas au serveur de contrôle sont toujours identiques.
#. La première information est le numéro du point d’accès dans le site.
#. La seconde information est le numéro du bissas dans ce point d’accès
#. La troisième information est la face sur laquelle le badge a été lu (A ou B).
#. La dernière information est le "bCode" (code badge) lu par le lecteur de badge.

#. A chaque fois qu'une porte est refermée, il détecte l'absence ou la présence d'une personne en retournant Void ou Full.