# Automate pour modéliser un système

## **Définition**
Un **automate** est un formalisme (ou outil mathématique) permettant de **modéliser** le comportement de certaines classes de systèmes qui interagissent avec leur environnement.

### **Exemples d'applications :**
- Distributeurs de boissons.
- Robots autonomes ou pilotes automatiques d’avion (systèmes de contrôle-commande).
- Digicodes.
- Programmes en cours d’exécution.
- Processeurs.

---

## **Modélisation**
La modélisation est utilisée pour **concevoir**, **comprendre** ou **simuler** un système complexe en construisant une **représentation simplifiée** (un modèle). Ce modèle ne retient que les aspects essentiels du système.

### **Domaines d'application :**
- Physique : mécanique, énergétique, thermique, etc.
- Électronique.
- Informatique.

---

## **Exemple : Distributeur de boissons**
Modélisation d’un distributeur de boissons très simple :
1. Le système attend de recevoir une pièce d’un euro.
2. L’utilisateur effectue un choix : thé ou café.
3. Le système sert la boisson choisie.

---

## **Algorithme de simulation**
Un automate peut être simulé à l’aide de l'algorithme suivant :

```c
etat_courant = Init;
while (!FINI) {
    entree = lire_entree();
    sortie = sortie(etat_courant, entree);
    etat_suivant = transition(etat_courant, entree);
    traiter_sortie(sortie);
    etat_courant = etat_suivant;
    mise_a_jour_de_FINI;
}
```
Fonctions de transition et de sortie
Plusieurs options
Forme fonctionnelle

```c
int transition(int etat_courant, char entree) {
switch (etat_courant) {
case 0:
switch (entree) {
case ’c’: return 0;
case ’1’: return 1;
...
```
Forme tabulee´
On remplit un tableau nomme´ transition, puis
etat suivant = transition[etat courant][entree];
Il faut que etat courant et entree soient des entiers
