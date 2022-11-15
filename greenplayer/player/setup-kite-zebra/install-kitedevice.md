# Install KiteDevice

1. Connecter le Zebra par USB type c a un pc qui a adb d’installer
2. Télécharger la [dernière release de l’apk](https://builds.kitedevice.com/) prendre la v7
3. Activer le débogage par USB sur le Zebra
   1. Aller dans les paramètres
   2. Aller tout en bas dans à propos
   3. Aller tout en bas jusqu’à numéro de build
   4. Cliquer sur le numéro de build jusqu’à ce qu’il y soit marqué “vous êtes déjà un développeur”
   5. Retour en arrière
   6. Aller dans système
   7. Paramètres avancés
   8. Options pour les développeurs
   9. Trouver débogage USB : Activer, Ok
   10. Un pop-up demandant d’autoriser apparait (si le Zebra est déjà branché à un pc, sinon il faut le brancher) : Autoriser l’appareil
4. Sur le pc ouvrir un cmd
5. Taper “**adb devices”**
6. Normalement un device apparait dans la liste
7. Se rendre avec le cmd dans le dossier où se trouve l’apk précédemment télécharger
8. Taper “**adb install kitedevice.apk**” (remplacer kitedevice.apk par le vrai nom du fichier)
9. Le cmd indique succès
10. Revenir sur le bureau du Zebra
11. Le Zebra demande quelle application utiliser comme écran d’accueil
    1. Sélectionner KiteDevice
12. KiteDevice s’ouvre et indique qu’il n’est pas le device owner
    1. Taper dans le cmd “**adb shell dpm set-device-owner com.kitedevice/.AdminReceiver**”
13. Kite device ce ferme
14. Revenir une nouvelle fois sur le bureau du Zebra avec le rond en bas
15. Le Zebra propose d’utiliser KiteDevice comme écran d’accueil : Toujours
16. KiteDevice se lance et afficher qu’il est prêt a l’utilisation
