#Commandes Git sur le terminal

##Importer un projet github :
##Voir les fichiers en attende de validation :

    > git status

##Valider un ou des fichier(s) :

    >git commit --all
## Interface à puce 
##supprimer tous les # des fichier à upload
>crtl x
>o
##Envoyer les fichiers validés en ligne :

    >git add --all
## Pour envoyer
    >git push origin maste

# installer jekyll
## installer ruby avant
sudo apt-get install ruby ruby-dev make gcc nodejs
##install jekyll
sudo gen install jekyll --no-doc --no-ri
#casser une commande
cmd+c
#lancer jekyll
jekyll serve
#aller dans le dossier sites
lancer le terminal et faire un jekyll serve 
## le includ 
templates
##_site
c'est ce qui est généré par jelyll -> pas toucher 
## dans congig on appel les includs 
title: documentation
## HTML
le html appel les includes via {% include "le fichier".html %}
##_includes
Dans les includes on met <title>{{ site."le fichier" }}</title>
##_layout
faire un fichier défault.html {{content}} -> liquid tag
#layout - gabarit
# permet de ne pas recopier du cote, surtout quadnd on a plein de page c'est chiant de tout refaire. On peut aussi faire du prototypage

# lancer jekyll
jekyll serve : on chop le lien en bas pour avoir notre site en local

# faire un menu "intelligent"
assign c'est la variable on a le tableau site .pages dans lequel on a toutes nos page: en gros on récupère le tableau qui devient un menu par ordre alphabétique.
# Dans default.md on remplace le menu par 
		<nav id="nav">
            {% assign pages = site.pages | sort:"weight"  %}
                    <ul>
                      {% for p in site.pages %}
                        <li>
                          <a href="{{ p.url }}">{{ p.title }}</a>
                        </li>
                      {% endfor %}
                </ul>
		</nav>
    
#créé des posts 
créé un dossier _posts dans lequel on met tout les postes 
article s'écrit année-moi-jour-titre.md
#créé un fichier à la racine:
posts.md et mettre 
< ul>
 > {% for post in site.posts %}
  >  < li>
   >   <a href="{{ post.url }}">{{ post.title }}</a>
    >  {{ post.excerpt }}
>    < /li>
>  {% endfor %}
</ ul>
#Fichier SASS
$color-primary:#AABBCC
body{
color:color.primary.
}
permet de générer des grilles.
#flexibox
> flex-wrap:Wrap
> display:flex (grid)

#css grid
permet de faire une grille, comme bootstap.

