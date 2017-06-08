# Compare_osm  
Compare deux fichiers OSM, l'un original, l'autre qui part du même et qui a été modifié à la main (sous JOSM, par exemple). Après comparaison, crée 3 fichiers de "diff" utilisé par le script to_renderer.py qui semi-automatise la réapplication de ces modifications.

# Utilisation

`python compare_osm.py infile_pre.osm infile_post.osm [rw]`

rw supprime les fichiers de différences pré-existants.  
3 fichiers incluant les différences sont créés, avec pour préfixe le nom du fichier d'entrée :  
* in_add.txt : tags ajoutés 
* in_delete.txt : tags supprimés
* in_offset.txt : décalage des nœuds.


# État des lieux
Semble globalement fonctionner, mais non testé dans des conditions extrèmes.  
Fonctionne notamment si les fichiers ne contiennent pas les mêmes objets. Si pre plus grand que post, pas d'avertissement. Si objet dans post absent de pré, affiche un avertissement (comparaison pré/post impossible).