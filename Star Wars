# -*- coding: utf-8 -*-
"""
Created on Fri Sep 16 12:27:28 2022

@author: KEIMADT
"""

class Film():
    
    #Constructeur
    def __init__ (self, Titre, Annee, Num, Cout, Recette, ListeActeur):
        self.titre = Titre
        self.annee = Annee
        self.numEp = Num
        self.cout = Cout
        self.recette = Recette
        self.listeActeur = ListeActeur
    
    #Setter
    def set_titre(self, Titre):
        self.titre = Titre
    
    def set_annee(self, Annee):
        self.annee = Annee
        
    def set_num(self, Num):
        self.numEp = Num
    
    def set_cout(self, Cout):
        self.cout = Cout
    
    def set_recette(self, Recette):
        self.recette = Recette
        
    def set_listeActeur(self, ListeActeur):
        self.listeActeur = ListeActeur
    
    #Getter
    def get_titre(self):
        return self.titre
    
    def get_annee(self):
        return self.annee
    
    def get_num(self):
        return self.numEp
    
    def get_cout(self):
        return self.cout
    
    def get_recette(self):
        return self.recette
    
    def get_listeActeur(self):
        return self.listeActeur
    
    #Affichage des attributs de l'objet
    def str(self):
        print("\nTitre: ", self.titre)
        print("Année de sortie: ", self.annee)
        print("Numéro d'épisode: ", self.numEp)
        print("Cout en $: ", self.cout)
        print("Recette en $ : ", self.recette)
        print("\nListe des acteurs: \n")
        for i in range (0,len(self.listeActeur)):
            Acteur.str(self.listeActeur[i])
        print("________________________________")
      
    #Affiche le nombre de role de l'acteur
    def nbActeur(self):
        nb = len(self.listeActeur)
        print("nombre d'acteur dans le film : ",nb)
    
    #Calcul si le film est rentable
    def calculBenefice(self):
        
        #Cas si le coût est inférieur aux recettes -> bénéfice
        if(self.cout < self.recette):
            resultat = self.recette - self.cout
            benefice = True
        
        #Cas si le coût est supérieur aux recettes -> déficit
        elif(self.cout > self.recette):
            resultat = self.cout - self.recette 
            benefice = False
        
        #Cas d'égalité entre le coût et les recettes -> pas de bénéfice
        else:
            resultat = 0
            benefice = False          
        return resultat, benefice
    
    #Calcul si le film est sortie avant l'année renseigné
    def isBefore(self, annee):
        if(self.annee > annee):
            booleen = False
        else:
            booleen = True
        return booleen
    
    #Trie les acteurs par ordre alphabétique
    def tri(self):
        dico = {}
        print("\nTri des acteurs par leur nom")
        for i in range (0,len(self.listeActeur)):           
            name = Acteur.get_nom(self.listeActeur[i])
            firstName = Acteur.get_prenom(self.listeActeur[i])
            dico[name] = firstName
            
        for j in sorted(dico.keys()):
            print("%s %s" % (j, dico[j]))
    
    #Affiche l'année, le titre et les bénéfices du film
    def makeBackUp(Dico):
        for cle, valeur in Dico.items():
            print("Année: ",cle, " - Titre: ", Film.get_titre(valeur), " - Bénéfice: ",Film.calculBenefice(valeur))
 
        
class Acteur():
   #Constructeur
    def __init__ (self, Nom, Prenom, ListeRole):
        self.nom = Nom
        self.prenom = Prenom
        self.listeRole = ListeRole
        
    #Setter
    def set_nom(self, Nom):
        self.nom = Nom
    
    def set_prenom(self, Prenom):
        self.prenom = Prenom
        
    def set_listeRole(self, ListeRole):
        self.listeRole = ListeRole
    
    #Getter
    def get_nom(self):
        return self.nom
    
    def get_prenom(self):
        return self.prenom
    
    def get_listeRole(self):
        return self.listeRole
     
     #Affichage des attributs de l'objet   
    def str(self):
        print("Nom: ", self.nom," | Prénom: ", self.prenom)
        print("Liste des roles :")
        for i in range (0,len(self.listeRole)):
            Personnage.str(self.listeRole[i])
        print("\n")
     
    #Affiche le nombre de role joué par l'acteur
    def nbPerso(self):
        nb = len(self.listeRole)
        print("nombre de role de l'acteur : ",nb)
    
    
            
    
class Personnage():
    
    #Constructeur
    def __init__ (self, Nom, Prenom):
        self.nom = Nom
        self.prenom = Prenom
        
    #Setter
    def set_nom(self, Nom):
        self.nom = Nom
    
    def set_prenom(self, Prenom):
        self.prenom = Prenom
    
    #Getter
    def get_nom(self):
        return self.nom
    
    def get_prenom(self):
        return self.prenom
    
    #Affichage des attributs de l'objet
    def str(self):
        print("Nom: ", self.nom," | Prénom: ", self.prenom)
    
    
class Gentil(Personnage):
    #Constructeur
    def __init__ (self, Force):
        self.force = Force
        
    #Setter
    def set_nom(self, Force):
        self.force = Force
    
    #Getter
    def get_nom(self):
        return self.force
    
    
class Mechant(Personnage):
    #Constructeur
    def __init__ (self, Obscur):
        self.obscur = Obscur
        
    #Setter
    def set_nom(self, Obscur):
        self.obscur = Obscur
    
    #Getter
    def get_nom(self):
        return self.obscur

    
#Initialisation objet Personnage

perso1 = Personnage("Han","Solo")
perso2 = Personnage("Skywalker","Rey")
perso3 = Personnage("Skywalker","Anakin")
perso4 = Personnage("Jones","Indiana")

#Affectation des roles joués par un acteur
acteur1Role = [perso1, perso4]
acteur2Role = [perso2]
acteur3Role = [perso3]

#Initialisation objet Acteur
acteur1 = Acteur("Ford","Harrison",acteur1Role)
acteur2 = Acteur("Ridley", "Daisy",acteur2Role)
acteur3 = Acteur("Christensen", "Hayden",acteur3Role)

#Initialisation des Listes des acteurs
ListeActeur1 = [acteur1, acteur2, acteur3]
ListeActeur2 = [acteur2, acteur3]
ListeActeur3 = []

#Initialisation d'objet Films
film1 = Film("Star Wars, Un nouvel espoir", 1977, "IV", 8000, 323000, ListeActeur1)    
film2 = Film("Star Wars, L'Empire contre-attaque", 1980, "V", 1000, 4000, ListeActeur2)

#Demande à l'utilisateur de saisir les données d'un film
#Ne demande pas la liste des acteurs, liste d'acteur initialisé par défaut
titre = input("Saisir le titre d'un film Star Wars : ")
annee = int(input("Saisir l'année de sortie de ce film : "))
num = input("Saisir le numéro d'épisode de ce film : ")
cout = int(input("Saisir le cout de ce film : "))
recette = int(input("Saisir les recettes de ce film : "))
film3 = Film(titre, annee, num, cout, recette, ListeActeur3)

#Initialisation des listes de films
ListeFilm1 = [film1, film2, film3]

#Initialisation dictionnaire de film
dicoFilm = {}

dicoFilm[Film.get_annee(film1)]=film1
dicoFilm[Film.get_annee(film2)]=film2
dicoFilm[Film.get_annee(film3)]=film3


#Affiche tous les films présents dans liste de films
def printListe(nomListe):
    for i in range (0,len(nomListe)):
        Film.str(nomListe[i])
printListe(ListeFilm1)

#test de la méthode Acteur.nbPerso()
Acteur.nbPerso(acteur1)

#test de la méthode Film.nbActeur()
Film.nbActeur(film1)

#Test de la méthode Film.calculBenefice() qui retourne un int et un bool
resultat1 = Film.calculBenefice(film1)
if(resultat1[1]==True):
    print(resultat1[1], ", le film est bénificiaire de ",resultat1[0],"$")
else:
    print(resultat1[1], ", le film est en décifit de ",resultat1[0],"$")

#Test de la méthode Film.isBefore() qui retourne un bool
resultat2 = Film.isBefore(film1, 1600)
print("Le film est sortie avant : ", resultat2)

#Test de la méthode Film.tri()
Film.tri(film1)

#Test fonction makeBackUp
Film.makeBackUp(dicoFilm)
