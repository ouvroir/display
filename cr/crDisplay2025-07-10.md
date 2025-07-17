---
title: "Réunion Tractr"
description: "Compte-rendu de la réunion hebdomadaire du 10 juillet 2025"
author: ouvroir
date: 2025-07-10
draft: false
tags:
    - cr 

---

Cablage de l'API est necessaire à ce point là. Glenn s'est posé sur cette problématique qui n'est pas simple. On a deux sources de back end différent. Le supa base permet de creer des champs a courts termes. Un switch sera possible vers l'ontologie. Pour le cote ontologie, besoin de savoir ou se brancher. Mais on ne voyait pas d'ou venait quoi. A cherché un moyen simple, flexible de faire tout ça. 

Libairie pour routes vers ontologie : Ok, plutot simple. 
Supabase : on avait un gros cache json pratique car flexible mais pas suffisant. Désormais, modélisation Supabase plus ou moins cablée sur l’ontologie

@rmq vraiment j'aime pas le principe des doublons.

Mais veut se permettre d’avoir des choses qui ne seront pas dans l’ontologie mais qui pourrait l’être plus tard.

Appelée bridge car dans les deux sens, la librairie va permettre de prendre les contenus, vérifier les changements et les pousser vers l’ontologie. Ou bien récupérer les sources, les répliquer et mettre à jour.

Plusieurs tests et itérations pour voir ce qui était le plus pratique. Une interface pour voir ce qui a été mis en dessous.
En même temps, en profite pour faire des corrections et améliorer ce qui peut l’être.

Le résultat n’est pas très visible (idem la fois avants). Mais dès que fait des changements bouton pour faire du débuguage (bridge history). Ouvre une liste de journalisation. Voit les patchs dans l’ontologie.

Reste qq pts bugs car des champs que l’API n’accepte pas dans les patch. Ex. Classified-as où une transformation entre la création et contexte qu’eessaye d’enlever.

David, champ contexte dont ne devrait pas avoir à s’occuper. Mais pas accepté dans la route de PUT.

Contexte juste une maniere de renvoyer semantique sur ce qu'on envoi. L'enlever des updates pour qu'on le voit pas puisque "pose probleme".

Un pt bug sur la création d’un set. David va regler ce petit problème de mapping.

Glenn utilise actuellement le serveur en prod. 
Prévoir un call David-Glenn pour regarder les ecritures sur le serveur ontologie.

La modélisation reste très plate même si elle est traitée en relationnel. Seule chose traitée en relationnel, les projets.

Terminer le chantier à faire.
Prochaine étape, reréfléchir au système de sources. D’abord une ptite version sans code. Prévoir réunion plus atelier pour ça. 

Sur le rétroplaning où se situe. Arthur revient fin de semaine prochaine pour plannification. Grosse feature à prévoir pour les sources. Ne pas négliger le travail sur les vues et les caméras qui sera déterminant pour l’attrait et l’usabilité de l’application. Finalisation à la rentrée.