;; README.de.txt                             -*- coding: latin-1; -*-
;; This is the README installed with Gpg4win (German version).  Lines
;; with a ; in the first column are considered a comment and not
;; included in the actually installed version.  Certain keywords are
;; replaced by the Makefile; those words are enclosed by exclamation
;; marks.

                  Deutsche README Datei f�r Gpg4win
                  =================================
!BETA-WARNING!
Dies ist Gpg4win, Version !VERSION! (!BUILD_ISODATE!).

Inhalt:

     1. Wichtige Hinweise
     2. �nderungen
     3. Bekannte Probleme (und Abhilfen)
     4. Installation
     5. Versionshistorie
     6. Versionsnummern der einzelnen Programmteile
     7. Rechtliche Hinweise


1. Wichtige Hinweise
====================

Hilfe bei der Installation und Benutzung von Gpg4win bietet Ihnen das
Gpg4win-Kompendium. Sie finden es nach der Installation im
Gpg4win-Startmen� unter 'Dokumentation' oder direkt online unter:
http://www.gpg4win.de/doc/de/gpg4win-compendium.html

Bitte lesen Sie den Abschnitt "3. Bekannte Probleme (und Abhilfen)"
dieses READMEs, bevor Sie beginnen Gpg4win zu nutzen.

Gpg4win unterst�tzt folgende Plattformen:

  * Betriebssystem: Windows XP und neuere Versionen (f�r alle: 32/64 bit)

  * MS Outlook: 2003, 2007, 2010, 2013, 2016 (2010 und sp�tere auch in 64bit)


2. �nderungen
=============

Die integrierten Gpg4win-Komponenten in Version !VERSION! sind:

!COMPONENTS!


Neu in Gpg4win Version !VERSION! (!BUILD_ISODATE!)
-----------------------------------------

- Es wird nun die moderne 2.1 Variante von GnuPG verwendet. Unter:
  https://www.gnupg.org/faq/whats-new-in-2.1.html (englisch)
  finden sich mehr details dazu.

- Die 64bit variante von Outlook wird nun von GpgOL unterst�tzt.

- GpgOL f�r Outlook 2010 und sp�tere Versionen verwendet nun
  schaltkn�pfe zur Auswahl ob eine Mail verschl�sselt und oder
  signiert sein soll. Die operation erfolgt w�hrend des versendens,
  dabei werden auch alle Anh�nge mitverschl�sselt und ein
  standartisiertes Format (MIME) verwendet.

- GpgOL f�r Outlook 2010 und sp�tere Versionen entschl�sselt nun
  wieder automatisch Mails.

- Alle 68 KDE �bersetzungen von Kleopatra werden nun mit Gpg4win
  installiert.

- Kleopatra verwendet ein aktualisertes Icon Set.

- Kleopatra zeigt nun die verwendete Kurve f�r ECC Schl�ssel in den
  Technischen Details an.

- Die von Kleopatra verwendeten Programmbibliotheken wurden aktualisiert.

- Ausf�hrbare Anwendungen werden nun im bin unterordner abgelegt. Die
  hilfsanwendungen DBus und kbuildsycoca werden nicht mehr ben�tigt.
  Dies l�st eine Reihe von Kleopatra startproblemen die bei Manchen
  Anwendern aufgetreten sind.

- Nach dem import eines geheimen Schl�ssels bietet Kleopatra nun gleich
  an diesen einen eignen Schl�ssel zu markieren. (Inhabervertrauen)

- Kleopatra bietet nun in den Erweiterten Optionen bei der
  Schl�sselerstellung an ECC Schl�ssel zu erstellen.

- Kleopatra bietet nun die Option einen Privaten Schl�ssel mit Paperkey zu drucken.

- Es ist nun auch m�glich �ber Kleopatras Dateimen� Ordner zu verschl�sseln.

- GPA und Kleopatra werden nun als Anwendungen f�r OpenPGP und S/MIME Dateiendungen in
  Windows registriert.

- Der Dateiverschl�sselungsdialog von Kleopatra wurde neu Entworfen um weniger
  Schritte zu enthalten und die Nutzererfahrung zu verbessern.

- Kleopatra erkennt nun automatisch um welche Dateiart es sich handelt und startet
  die entsprechende Aktion (z.B. entschl�sseln) automatisch.

- Symmetrische (nur mit Passwort) verschl�sselung kann nun auch �ber Kleopatra
  durchgef�hrt werden und mit Public-Key-Verschl�sselung kombiniert werden.

- Pinentry erlaubt es nun die eingegebene Passprhase anzuzeigen.

3. Bekannte Probleme (und Abhilfen)
===================================

- Smartcard-Nutzung mit Kleopatra

   Die Einrichtung von Smartcards unter Kleopatra ist derzeit noch
   nicht vollst�ndig m�glich. Bitte f�hren Sie folgende Schritte
   einmalig durch, um Ihre Smartcard anschlie�end unter Kleopatra
   nutzen zu k�nnen.

   * OpenPGP Karte
     Verwenden Sie das gpg-Kommandozeilen-Werkzeug, um ein neues
     OpenPGP-Zertifikat auf Ihrer Karte zu erzeugen (a) oder Ihr
     vohandenes Zertifikat von Ihrer Karte zu aktivieren (b):

     (a) Neues Zertifikat erzeugen
       - Karte einlegen.
       - F�hren Sie "gpg --card-edit" auf der Kommandozeile aus.
       - Wechseln Sie in den Admin-Modus mit "admin".
       - Geben Sie "generate" ein und folgen Sie den Anweisungen, um
         ein neues Zertifiakt zu erzeugen.

     (b) Vorhandenes Zertifikat von der Karte aktivieren
       - Das (zu der Karte) zugeh�rige �ffentliche Zertifikat
         importieren (z.B. von einem Zertifikatsserver oder von einer
         vorher exportierten Zertifikatsdatei).
       - Karte einlegen.
       - F�hren Sie "gpg --card-status" auf der Kommandozeile aus.

   * X.509 Telesec Netkey 3 Karte
     Verwenden Sie Kleopatra, um Ihre Karte (einmalig) zu initialisieren:
     - Karte einlegen.
     - Auf das blinkende Kleopatra-Smartcard-Systemtray-Icon klicken
       (oder direkt das Systemtray-Kontextmen� "Smartcard" und dort
       den "LearnCard"-Eintrag aufrufen).

   Anschlie�end wird Ihr OpenPGP- bzw. X.509-Smartcard-Zertifikat in
   Kleopatra unter dem Reiter "Meine Zertifikate" angezeigt (markiert
   mit einem Smartcard-Icon).

- Verwendung der Outlook-Programmerweiterung "GpgOL":

  * Sie sollten unbedingt vor der Installation von GpgOL
    Sicherheitskopien Ihrer alten verschl�sselten/signierten E-Mails
    erstellen, z.B. in PST-Dateien!

  * Nur f�r Outlook 2003/2007:
    Senden von signierten oder verschl�sselten Nachrichten �ber ein
    Exchange-basiertes Konto funktioniert nicht.
    [siehe https://bugs.g10code.com/gnupg/issue1102]
    (Hinweis: Beim Verwenden von SMTP sollte das Senden
     mit GpgOL funktionieren. Oder Sie nutzen GpgOL mit Outlook
    2010/2013.)

  * Nur f�r Outlook 2003/2007:
    Verschl�sselte E-Mails unverschl�sselt auf E-Mail-Server:
    Es kann vorkommen, dass Teile von verschl�sselten E-Mails
    in entschl�sselter/unverschl�sselter Form auf dem E-Mail-Server
    (IMAP oder MAPI) zu liegen kommen, wenn man sie erstellt/liest.
    Betroffen sind nur der Inhalt des Anzeigefensters von Outlook,
    also der "E-Mail-Body".  Anh�nge sind nicht betroffen.
    Schaltet man die Voransicht von Outlook ab, so
    verringert sich die Wahrscheinlichkeit daf�r deutlich,
    aber es kann trotzdem noch passieren. Oder Sie nutzen GpgOl mit
    Outlook 2010/2013.


4. Installation
===============

Eine Anleitung zur Installation von Gpg4win finden Sie im Gpg4win-Kompendium:
http://www.gpg4win.de/doc/de/gpg4win-compendium_11.html

Hinweise zur automatisierten Installation (ohne Benutzerdialoge)
finden Sie im Anhang des Gpg4win-Komendiums:
http://www.gpg4win.de/doc/de/gpg4win-compendium_35.html


5. Versionsgeschichte
=====================

Eine aktuelle deutschsprachige �bersicht der �nderungen finden Sie online
unter: http://www.gpg4win.de/change-history-de.html
Im weiteren finden Sie die Eintr�ge aus der englischen NEWS-Datei:

!NEWSFILE!


6. Versionsnummern der einzelnen Programmteile
==============================================

Zur �bersicht sind hier die Pr�fsummen sowie die Namen der einzelnen
Bestandteile aufgelistet.

!VERSIONINFO!


7. Rechtliche Hinweise zu den einzelnen Bestandteilen der Software
==================================================================

Gpg4win besteht aus einer ganzen Reihe von unabh�ngig entwickelten
Packeten, die teilweise unterschiedliche Lizenzen haben.  Der Gro�teil
dieser Software ist, wie Gpg4win selbst, steht unter der GNU General
Public License (GNU GPL).  Gemeinsam ist, dass die Software ohne
Restriktionen benutzt werden kann, ver�ndert werden darf und
�nderungen weitergeben d�rfen.  Wenn die Quelltexte (also
gpg4win-x.y.z.tar.bz2) mit weitergegeben werden und auf die die GNU
GPL hingewiesen wird, ist die Weitergabe in jedem Fall m�glich.

Zur �bersicht folgt eine Liste der Copyright Erkl�rungen.


!PKG-COPYRIGHT!




Viel Erfolg,

  Ihr Gpg4win Team


*** Ende der Datei ***
