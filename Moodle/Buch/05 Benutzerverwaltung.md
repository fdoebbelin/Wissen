Was wäre eine Lernplattform ohne Lernende und ohne Lehrende? Lehrende erstellen und verwalten in einem elektronischen Lernsystem Kurse. Lernende finden hier Unterrichtsmaterial und geführte Lektionen, aber auch Kontaktmöglichkeiten zu den Lehrenden und anderen Mitlernenden.

Lernende und Lehrende sind jeweils Benutzer dieses Systems. Bevor diese Personen aktiv werden können, müssen sie dem Moodle-System beitreten und eine Rolle in diesem digitalen Mikrokosmos zugewiesen bekommen. Wie die Benutzer Teil des Systems werden und welche Rollen sie einnehmen dürfen, legt die Adminis tration fest.

![](index-150_1.jpg)
**Bild 5.1** Der Moodle-Administrator hat entscheidenden Einfluss auf die Aktivitäten der Benutzer und deren Rollen im System.

**128** 5 Benutzerverwaltung

**■**

**■ 5.1■Neuer Benutzer/neue Benutzerin**

Um dem Moodle-System beizutreten, gibt es verschiedene Möglichkeiten. In komplexen Netzwerkinfrastrukturen können Benutzerinnen und Benutzer beispielsweise über einen zentralen Server in das System aufgenommen werden und sich über diesen direkt auch an Moodle anmelden. Dies ist beispielsweise der Fall, wenn Moodle in Unternehmen zur internen Fortbildung von Mitarbeitern oder an Schulen oder Hochschulen eingesetzt wird, wo Lernende und Studierende bereits einen Zugang zum Campussystem haben. In diesem Fall kann Moodle mit der Aktivierung entsprechender Plugins auf einen LDAP-Server bzw. ein anderweitiges Single Sign On-(SSO)-System zugreifen.

Im Folgenden soll Moodle allerdings eigenständig betrachtet werden. Dazu werden zwei Möglichkeiten vorgestellt, Benutzerinnen und Benutzer in das System zu integrieren.

Selbstanmeldung per E-Mail

Aufnahme durch die Administration

**5.1.1■Selbstanmeldung per E-Mail**

Die Selbsteinschreibung in das Moodle-System stellt eine erhebliche Entlastung der Ad -

ministration dar und beschleunigt nicht zuletzt auch die Abwicklung von Kursen. Wollen Lehrende ihren Lernenden Material zur Verfügung stellen, während des Unterrichts elektronisches Feedback einholen oder Lernzielkontrollen durchführen, so sind dazu ein Moodle- Zugang und die Aufnahme in einen Kurs erforderlich. Lediglich die Aufnahme in den Kurs kann der Lehrende (Teacher) vollziehen. Um aktiv Teilnehmerinnen und Teilnehmer in dem Moodle-System zu registrieren, fehlt dieser Person meist die Berechtigung.

Spontane Lösungen sind ohne Selbsteinschreibung also nicht möglich.

Allerdings gibt es auch Argumente, die gegen eine Selbsteinschreibung sprechen. So wird beispielsweise eine Überflutung des Systems mit _Fakeprofilen_ als Risiko gesehen.

Damit sich Personen im Moodle-System selbst registrieren können, müssen durch die Administration die entsprechenden Voraussetzungen geschaffen werden.

**Grundeinstellung: Keine Selbsteinschreibung!**

Unmittelbar nach der Neuinstallation eines Moodle-Systems ist es nicht

möglich, dass sich Benutzerinnen und Benutzer des Systems selbst ein-

schreiben können. Dies muss erst ausdrücklich zugelassen werden.

■

![Image 96](index-152_1.jpg)

5.1 Neuer Benutzer/neue Benutzerin

**129**

**5.1.1.1■Schritt 1: Website-Administration: Plugins**

Die Erlaubnis zu erteilen, dass sich Benutzer selbstständig mit der Angabe ihrer E-Mail-Adresse in das Moodle-System einschreiben können, ist _nicht_ Teil der Benutzerverwaltung.

Dies geschieht in der Verwaltung der Plugins.1 Dort gibt es eine Fülle von Abschnitten, nach denen Plugins im System eingeordnet werden können:

Plugins (Übersicht und Installation)

Aktivitäten (diese Plugins werden eine Bedeutung für die Möglichkeiten der _Teacher_ zur Gestaltung ihrer Lerneinheiten haben)

Antivirus-Plugins

Authentifizierung (hier soll die Selbsteinschreibung ermöglicht werden)

. . .

Einschreibung (dies bezieht sich auf die Einschreibung von Students in bestehende Kurse)

und viele mehr.

Im Bereich _Authentifizierung_ muss der Link _Übersicht_ gewählt werden! Darin findet man zunächst einmal tatsächlich eine Übersicht über die aktiven Plugins, die für Authentifizie-rungsaufgaben genutzt werden.

**Bild 5.2** Über diese Seite kann man sich nicht selbst im Moodle-System registrieren. Es ist lediglich möglich, sich mit bereits vorhandenen Zugangsdaten oder als „Gast“ anzumelden.

Bild 5.3 zeigt, dass das Plugin für die E-Mail-basierte Authentifizierung aktiviert wurde. Ein Klick auf „das Auge“ deaktiviert dieses Plugin! Um die Funktion zu aktivieren, sind aller-1 Plugins sind Erweiterungen des Moodle-Basissystems um verschiedene anwendungsorientierte oder systeminterne Funktionen. Auch viele Standardkomponenten sind als Plugins bereits fest in das System integriert, andere können nahezu beliebig nachträglich installiert werden.

![Image 97](index-153_1.jpg)

![Image 98](index-153_2.jpg)

**130** 5 Benutzerverwaltung

dings zwei Schritte erforderlich: Einerseits muss das Plugin _aktiv_ gesetzt werden. Darüber hinaus muss aber auch in den _Grundeinstellungen_ (etwas weiter unten in der gleichen Menüseite) die _Selbstregistrierung_ als „E-Mail basiert“ festgelegt werden. Damit die Einstellungen wirksam werden, müssen die Änderungen gesichert werden (blaue Schaltfläche ganz unten in der Seite). Dies gilt grundsätzlich bei jeder Konfigurationsänderung.

**Bild 5.3** Das Plugin für die E-Mail-basierte Authentifizierung muss aktiv gesetzt sein. Hier ist auch deutlich zu erkennen, dass dieses Moodle-System keine externen Authentifizierungs verfahren (SSO, LDAP etc.) benutzt, da diese Plugins nicht aktiv gesetzt sind.

**Bild 5.4** In den Grundeinstellungen muss ausdrücklich die „E-Mail basierte“ Selbstregistrierung gewählt werden. Erst dann erscheint der entsprechende Dialog auf der Login-Seite.

5.1 Neuer Benutzer/neue Benutzerin

**131**

Ein erneuter Aufruf der Moodle-Homepage und des Login-Dialogs zeigt die Änderung an: Wer noch keinen Zugang zum System hat, wer also „das erste Mal auf dieser Seite ist“, kann jetzt ein neues Konto anlegen. Dazu werden einige persön liche Informationen benötigt. Dies sind ein selbstgewählter Benutzername, ein Kennwort und eine (gültige!) E-Mail-Adresse.

**5.1.1.2■Selbstregistrierung mit E-Mail-Adresse**

Wenn die Voraussetzungen gegeben und das erforderliche Plugin sowie die _E-Mail-basierte_ _Selbstregistrierung_ aktiviert sind, bietet sich dem Besucher der Moodle- Login-Seite ein anderes, erweitertes Bild: Es wird eine Schaltfläche zum Anlegen eines neuen Kontos2 angeboten.

Für ein neues Benutzerkonto werden gleich zu Beginn verschiedene Informationen abgefragt. Einige davon sind Pflichtangaben, ohne die kein Benutzerkonto erstellt werden kann.

Das betrifft übrigens nicht nur die individuell zu wählenden Zugangsdaten, sondern auch Vor- und Zuname sowie eine gültige E-Mail-Adresse. Ohne eine E-Mail-Adresse kann die Anmeldung nicht durchgeführt werden, weil Moodle eine E-Mail versendet. Diese enthält einen Code, der zur Bestätigung verwendet wird. Auf diese Weise wird es erheblich erschwert, dass das System von SPAM-Bots angegriffen und gestört wird.

**Moodle und E-Mail-Kommunikation**

Damit der Versand der Bestätigungsmail und der Empfang der Antwort durch das Moodle-System automatisch erfolgen kann, muss sowohl ein E-Mail-Eingang als auch ein E-Mail-Ausgang konfiguriert werden. Wie das funktioniert, beschreibt das Kapitel „E-Mail-Kommunikation“.

■

Bei den Zugangsdaten sollten die angehenden Benutzerinnen und Benutzer dringend darauf hingewiesen werden, ein _sicheres Passwort_ und einen _beliebigen Benutzernamen_ zu wählen. Diese Anweisung gehört durchaus in ein Informationsdokument, was allen Lernenden (und Lehrenden) bei Eintritt in die Schule/Hochschule bzw. das Bildungsinstitut aus-gehändigt werden kann. Die Sicherheitsregeln sollten eigentlich zum Allgemeinwissen gehören, jedoch zeigt die Praxis eher das Gegenteil.

**Zugangsdaten haben eine wichtige Schutzfunktion**

Nicht nur das Kennwort sollte sicher sein, auch der Anmeldename sollte so gewählt werden, dass damit keine „Scherze“ gemacht werden können, was

zur Sperre eines Benutzerkontos führen kann.

Die Systemadministration kann direkten Einfluss auf die Mindestvorgaben

bei Länge und die Zusammenstellung eines Kennworts ausüben. Dies wird in Abschnitt 5.2 beschrieben.

■

2 Selbstverständlich ist hier nicht von einem Bankkonto die Rede, sondern es handelt sich um die Mitgliedschaft im Moodle-System. Ob der Anbieter damit Kosten, Kündigungspflichten etc. verbindet, wird in der Regel separat geregelt. Darüber hinaus muss in einem solchen Fall ausdrücklich darauf hingewiesen werden. In den hier gezeigten Beispielen ist der Beitritt zum Moodle-System selbstverständlich _nicht_ mit Zahlungen oder sonstigen Verpflichtungen verbunden.

![Image 99](index-155_1.jpg)

**132** 5 Benutzerverwaltung

**Bild 5.5** Wenn dieses Bild auf der Login-Seite erscheint, kann man unter Angabe der eigenen E-Mail-Adresse ein eigenes Benutzerkonto innerhalb des Moodle-Systems anlegen. Eine Zuweisung zu Kursen ist damit allerdings noch nicht gegeben.

Zu den geforderten Daten gehören zusätzlich der Vor- und Zuname, wobei dieses Mal tatsächlich Realnamen gemeint sind. Auch diese sind verpflichtend einzutragen, weil sonst die Benutzerin bzw. der Benutzer in den einzelnen Lehrveranstaltungen keiner Person zugeordnet werden kann. Insbesondere bei Fernstudien, in denen die Ergebnisse der Lehrveranstaltungen auch rechtlich verbindlich sein müssen, ist eine klare persönliche Identifi-zierung erforderlich.

Nach der Eingabe dieser Daten und der Bestätigung des – per E-Mail verschickten – Codes wird das Konto aktiviert. Damit ist der Zugang zum Moodle-System und eine Einschreibung in die Kurse möglich. Für die Einschreibung in Kurse gibt es wiederum verschiedene Möglichkeiten:

Einschreibung durch den Lehrenden (Teacher)

Selbsteinschreibung

Mit der Aktivierung gelangt der neue Benutzer bzw. die neue Benutzerin auf die persönliche Startseite mit dem _Dashboard_. Bild 5.10 zeigt ein noch leeres Dashboard. Das liegt nicht nur daran, dass es sich neben dem Administrator um den ersten Benutzer im System handelt, sondern auch daran, dass der neuen Benutzerin bzw. dem neuen Benutzer noch keine Kurse zugewiesen sind. Die Kurse stellen die eigentlichen – in sich thematisch und auf einen definierten Teilnehmerkreis fokussierten – Lernbereiche dar. Auf das Dashboard wird in der „Moodle-Übersicht“ näher eingegangen.

![Image 100](index-156_1.jpg)

![Image 101](index-156_2.jpg)

5.1 Neuer Benutzer/neue Benutzerin

**133**

**Bild 5.6■**Zu den einzugebenden Pflichtdaten gehört neben den gewünschten Zugangsdaten vor allem eine E-Mail-Adresse. An diese wird eine Bestätigungsmail geschickt. Vor- und Zuname ( Realname!) sind für den Bezug zu den regulären Lehrveranstaltungen von Bedeutung.

**Bild 5.7** Nach Eingabe der benötigten Daten sendet Moodle eine E-Mail an die genannte Adresse.

Erst nach deren Bestätigung wird das Konto aktiviert.

![Image 102](index-157_1.jpg)

![Image 103](index-157_2.jpg)

**134** 5 Benutzerverwaltung

**Bild 5.8** Die Bestätigungs-E-Mail beinhaltet einen Link auf die Moodle-Seite. Dieser wird um einen Bestätigungscode ergänzt, den Moodle direkt auswerten kann. Erst nach Aufruf dieser Webadresse wird das Konto aktiviert.

**Bild 5.9** Das Moodle-Konto ist nun aktiviert. Mit der Schaltfläche „Weiter“ gelangt das neue Moodle-Mitglied zum persönlichen Dashboard.

![Image 104](index-158_1.jpg)

5.1 Neuer Benutzer/neue Benutzerin

**135**

**Bild 5.10** Das noch leere Dashboard ähnelt dem des Administrators nach der ersten Anmeldung, allerdings fehlt hier der Menüpunkt „Website-Administration“.

**5.1.2■Anmeldung durch Administrator**

Die Anmeldung durch den Administrator ermöglicht eine kontrollierte und organisierte Einladung von Benutzerinnen und Benutzern. Dies ist ergänzend zur Selbstregistrierung aber auch exklusiv möglich. Die Administration kann hier bereits vollständige Benutzerprofile anlegen. Der Vorteil dieser Methode ist, dass ausschließlich befugte Personen Zugang zum Moodle-System erhalten. Die Aufnahme in das Moodle-System kann beispielsweise Teil des administrativen Prozesses einer Immatrikulation sein. Der Nachteil ist, dass bei einer sehr großen Zahl Studierender bzw. Lernender der Verwaltungsaufwand sehr groß wird und sich dies tatsächlich signifikant in Arbeitsstunden und dafür zu entrichtende Entgelte als Kosten rechnen lässt.

In der Regel wird die Registrierung über die Administration deswegen vorzugsweise durch Lehrende oder direkt aktiv verwaltendes Personal vorgenommen, wobei diesen Personen auch gleichzeitig die entsprechenden Rollen und Rechte im System zugewiesen werden.

**Administrative Anmeldung verursacht Kosten!**

Die Verwaltung des Moodle-Systems ist grundsätzlich zeitaufwendig und

verursacht damit Personalkosten! Wenn Prozesse auf die Teilnehmerinnen

und Teilnehmer direkt delegiert werden können, spart das Kosten in einem signifikanten Ausmaß! Allerdings kann diese Einsparung kompensiert werden, wenn Nachbearbeitungen – beispielsweise Rollen- und Rechtezuweisungen –

für neu eingeschriebene Benutzerinnen und Benutzer zu leisten sind.

![Image 105](index-159_1.jpg)

![Image 106](index-159_2.jpg)

**136** 5 Benutzerverwaltung

Möglicherweise sind von diesen Personen Rückfragen zu beantworten.

In diesen Fällen kann sich die zentrale Aufnahme von Benutzerinnen und

Benutzern des Systems als vorteilhaft erweisen.

■

**Bild 5.11** Die Moodle-Administration kann direkt ein Benutzerkonto einrichten und die Zugangsdaten der betreffenden Person aushändigen.

**Bild 5.12** Es gelten auch hier die Kennwortregeln, die als Mindestanforderung im Interesse der Systemsicherheit zu beachten sind.

5.1 Neuer Benutzer/neue Benutzerin

**137**

Im Gegensatz zu verschiedenen anderen sozialen Communities ist Moodle keine Spaß- oder Vernetzungsplattform. Hier werden Bildungsinhalte bereitgestellt und Lernergebnisse überprüft. Letzteres soll jedoch nicht nur als persönliches Feedback dienen, sondern tatsächlich in eine Gesamtbewertung der Lernerfolge – gebildet aus Praxis, Präsenz- und Online-Unterricht – einfließen. Deswegen ist eine eindeutige persönliche Zuordnung erforderlich, wodurch der Vor- und der Zuname bei der Registrierung zu den Pflichtfeldern ge -

hören.

**Individuelle Profilgestaltung?**

In diesem Abschnitt geht es darum, Benutzerinnen und Benutzer in das

Moodle- System aufzunehmen. In diesem Zusammenhang drängt sich natürlich die Frage auf, ob tatsächlich alle Felder in dieser Form benötigt werden und wie flexibel Moodle ist, wenn weitere Daten in das Profil eingetragen werden sollen, wie beispielsweise eine Matrikelnummer etc. Auf die Details dazu geht Abschnitt 5.3 ein.

■

Selbstverständlich benötigen auch die durch die Administration eingerichteten Benutzerinnen und Benutzer ein sicheres Kennwort für den Zugang zum System. Hier gibt es zwei Möglichkeiten, dieses festzulegen:

Das System legt ein Zufallskennwort fest.

Die Administration legt ein willkürliches Kennwort fest.

Für die Gestaltung des Kennworts gelten auch bei der administrativen Einrichtung des Benutzerkontos die gleichen Bedingungen wie bei der Selbstregistrierung. Diese Regeln können nur von der Administration verändert werden (vgl. Abschnitt 5.2).

Wenn das Kennwort durch die Administration (manuell) vorgeschlagen wird, _kann_ zusätzlich eine Kennwortänderung bei der ersten Anmeldung erzwungen werden. Wird das Kennwort vom System erzeugt und der neuen Benutzerin bzw. dem neuen Benutzer per E-Mail zugestellt, so ist die Änderung des Passworts mit der ersten Anmeldung obligatorisch!

**E-Mail entspricht einer „Postkarte“!**

Per E-Mail versendete Nachrichten werden grundsätzlich offen und unver-

schlüsselt übertragen! Die Inhalte einer E-Mail sind also theoretisch für jedermann lesbar. Aus diesem Grund sind per E-Mail übermittelte Kennwörter als unsicher einzustufen. Zusätzliche Verschlüsselungsverfahren sind zwar möglich und bieten eine gewisse Sicherheit, sie gehören allerdings

nicht zum Standard in der E-Mail-Kommunikation.

■

Die Eingabe der E-Mail-Adresse ist in Moodle grundsätzlich Pflicht. Obwohl (theoretisch!) auf E-Mail-Benachrichtigungen bei Forenaktivitäten oder zur Benutzerregistrierung verzichtet werden könnte, würde dies die Nutzungsmöglichkeiten des Systems derartig einschränken, dass mangels Kommunikation kein sinnvoller Lehrbetrieb möglich wäre. Das bedeutet allerdings nicht zwangsweise, dass die E-Mail-Adresse allgemein bekannt gegeben

**138** 5 Benutzerverwaltung

werden und für jedermann sichtbar sein muss. Mit der Einrichtung des Benutzerkontos entscheidet jede Benutzerin und jeder Benutzer, für wen die Adresse sichtbar ist:

Grundsätzlich für alle

Nur für privilegierte Personen (Teacher, Administration)

Für Kursteilnehmerinnen und Kursteilnehmer

Die Administration kann an dieser Stelle bereits weitere Daten in das Profil einfügen. Insbesondere bei Lehrenden in großen Bildungseinrichtungen stellt ein aktuelles Profilfoto eine Brücke zwischen Lehrenden und Lernenden her. Zu beachten ist jedoch, dass stets das Recht am eigenen Foto gewahrt bleiben muss. Die Administration darf also nicht ein be -

liebiges Foto der Benutzerin oder des Benutzers in das System hochladen. Auch müssen die Betroffenen grundsätzlich damit einverstanden sein.

Weitere Daten wie das Land oder die Zeitzone und die Sprache sind dann wichtig, wenn es sich um eine internationale Lehrplattform handelt. So gibt es Fernhochschulen, in denen sowohl die Studierenden als auch die Lehrenden auf allen Kontinenten der Welt beheimatet sein können. Hier erleichtern diese Informationen die Kommunikation und die Planung von Live-Veranstaltungen.

Persönliche Interessen gehören eigentlich nicht in ein Personalprofil. Dies gilt jedenfalls für Mitarbeiterprofile in Unternehmen. In einer Lehrplattform kann es jedoch anders gesehen werden, denn insbesondere dann, wenn ein großer Schwerpunkt auf E-Learning gelegt und die Präsenzphasen eher gering gehalten werden, können Kenntnisse über gemeinsame persönliche Interessen durchaus ein soziales Miteinander der Studierenden fördern. Diese Angaben sind selbstverständlich auf rein freiwilliger Basis einzutragen.

**Studierendengruppen fördern Lernerfolge**

Lernende, die sich über die örtliche Nähe und gemeinsame Interessen auch privat kennenlernen und außerhalb der Lehrplattform kommunizieren, erreichen meist gemeinsam bessere Lernerfolge und motivieren einander. Diese

Tendenzen sollten von einer digitalen Lernplattform unterstützt werden!

■

![Image 107](index-162_1.jpg)

![Image 108](index-162_2.jpg)

5.1 Neuer Benutzer/neue Benutzerin

**139**

**Bild 5.13** Datenschutz ist wichtig, aber die Angabe einer gültigen E-Mail-Adresse ebenso. Die Benutzerin bzw. der Benutzer können jedoch Einfluss nehmen, wer die E-Mail-Adresse sehen darf.

**Bild 5.14** Wenn Details bereits vorhanden sind, können diese sowie ein Profilfoto bereits durch die Administration in das Profil eingefügt werden.

![Image 109](index-163_1.png)

**140** 5 Benutzerverwaltung

**Bild 5.15** Die Zugangsdaten wurden automatisch vom Moodle-System generiert. Aus Sicherheitsgründen muss das Kennwort allerdings von der Benutzerin bzw. dem Benutzer bei der ersten Anmeldung geändert werden.

**Den E-Mail-Text ändern?**

Der Text der E-Mail kann individuell und persönlicher gestaltet werden. Dazu muss der entsprechende Eintrag im Sprachpaket bearbeitet werden. Dieses

ist über die Moodle-Website-Administration zugänglich:

_Website-Administration – Sprache – Sprachanpassung – Filtertexte_

Hier wird in der Komponenten-Rubrik _core – moodle.php_ gesucht:

_**newusernewpasswordtext**_

■

**5.1.3■ Weitere Authentifizierungs- und Registrierungsverfahren**

Wird Moodle – wie in diesem Demo-System – ausschließlich isoliert betrachtet, werden die Zugänge mit den beschriebenen Verfahren die Regel sein. Ein exklusiver Zugang zu Moodle – unabhängig von eventuell bestehenden Campus-Netzwerken – ist allerdings oft aus Gründen der Sicherheit gewünscht. Nicht immer führt dies zur „Begeisterung“ bei den Benutzerinnen und Benutzern, die einen gemeinsamen Zugang zu allen Systemen des Instituts, der Schule oder Hochschule wünschen.

![Image 110](index-164_1.png)

5.1 Neuer Benutzer/neue Benutzerin

**141**

Je nachdem, wie die internen IT-Architekturen gestaltet sind, wird es verschiedene Technologien geben, für die Moodle mithilfe spezieller Plugins Schnittstellen anbieten muss. An dieser Stelle soll eine Auswahl der wichtigsten Verfahren genannt werden:

LTI® – Learning Tools Interoperability

LDAP – Lightweight Directory Access Protocol

CAS-Server – Central Authentication Service

**Bild 5.16** 

In diesem Demonstrationssystem sind

lediglich die E-Mail-basierte und die

manuelle Authen tifizierung aktiviert.

Universitäten, große Schulen und

Institute mit einer gut strukturierten

IT-Abteilung bieten jedoch weitere

Plattformen an, die mit dem Moodle-

System kooperieren und auf die

Benutzerkonten gemeinsam zu greifen

können.

**5.1.3.1■LTI® – Learning Tools Interoperability**

Das IMS3 Global Learning Consortium in Lake Mary, Florida, hat sich zum Ziel gesetzt, Lerntechnologien zu fördern, die kostengünstig weiterentwickelt werden können und dazu beitragen, die Akzeptanz von Lehrangeboten und das Erreichen der Lernziele zu verbessern. Mithilfe des LTI-Tools, welches seit der Version Moodle 2.2 verfügbar ist, können externe, jedoch LTI-kompatible Lehrwerkzeuge in die Moodle-Plattform integriert werden.

Von Bedeutung ist dies vor allem, weil Moodle-Kurse aus fremden Systemen über die LTI-Authentifizierung Teil eigener Kurse werden können. Diese werden als _Externes Tool_ in den Kurs eingefügt.

3 Das Instructional Management System (IMS) war ein Projekt der amerikanischen National Learning Infrastructure Initiative. Dieses Projekt geht bereits auf das Jahr 1977 zurück.

![Image 111](index-165_1.jpg)

![Image 112](index-165_2.jpg)

**142** 5 Benutzerverwaltung

**Bild 5.17** Die Aktivierung des LTI-Plugins erfolgt durch die Administration in der „Website-Administration“: Bereich _Plugins/Authentification/Übersicht_

**Bild 5.18** LTI muss für die Einschreibung aktiviert werden, damit externe Tools zur Verfügung gestellt bzw. genutzt werden können.

5.1 Neuer Benutzer/neue Benutzerin

**143**

Um auf eine Lektion bzw. einen Kursinhalt zuzugreifen, sind ein direkter Link und ein Security-Code notwendig. Beides muss dem jeweiligen Teacher bekannt sein. Students nutzen das Lehrangebot wie ein regulärer Bestandteil des Kurses.

**5.1.3.2■LDAP – Lightweight Directory Access Protocol**

Verzeichnisdienste in verteilten Netzwerken stellen hierarchische Datenstrukturen dar.

Diese können unter anderem personenbezogene Benutzerdaten – auch Zugangsdaten –

sowie Informationen zu den individuellen Arbeitsplätzen enthalten. Anhand dieser Informationen ist es beispielsweise möglich, sich in größeren Unternehmensnetzwerken an beliebigen Arbeitsplätzen anzumelden und stets eine vertraute Arbeitsumgebung vorzu-finden. Die Kommunikation mit diesen Verzeichnisdiensten erfolgt über spezielle Protokolle. Das Lightweight Directory Access Protocol (LDAP) ist ein solches Protokoll.

LDAP kommt in der Active-Directory-Architektur von Microsoft zum Einsatz. Hier werden tatsächliche Benutzerdaten, deren Gruppenzugehörigkeiten und Informationen zu den Arbeitsplätzen erfasst. Existiert eine Active-Directory-Infrastruktur, sollte über eine mögliche Kombination mit dem Moodle-System nachgedacht werden.

**Nicht zwingend alle Lernenden in das Active Directory einbinden**

Die LDAP-Authentifizierung ist lediglich eine Möglichkeit, sich im Moodle-System anzumelden. Es ist zu empfehlen, wenn das eigene Personal der

Schule bzw. des Instituts Zugang zu Moodle bekommen soll. Die Lernenden

selbst benötigen jedoch in der Regel keine weiteren Elemente der haus-

eigenen Infrastruktur.

■

**5.1.3.3■CAS – Central Authentication Server**

Moderne IT-Infrastrukturen bestehen aus verschiedenen Diensten, die auf unterschiedlicher Hardware und zum Teil an unterschiedlichen Orten laufen. Gemeinsame Basis ist das Netzwerk. Sehr ärgerlich und zudem zeitaufwendig ist es, wenn man sich an jedes System separat anmelden muss. Das bedeutet Zeitaufwand für die Anmeldeprozeduren, die sich durchaus mehrmals am Tag wiederholen können, wenn ein zeitgesteuerter Logout (Session Timeout) erfolgt, und erfordert möglicherweise auch, sich mehrere Zugangsdatensätze zu merken. Das Chaos ist perfekt, wenn diese Zugangsdaten verwechselt werden.

Sogenannte Single Sign On-(SSO)-Lösungen bieten Abhilfe. Hier übernimmt ein zentraler Authentifizierungsserver (Central Authentication Server) die Aufgabe des „Türstehers“.

Der Dienst ist dabei webbasierend und so für verschiedene Plattformen einsetzbar, wenn sie CAS unterstützen.

Für die Anmeldung wird die Benutzerin bzw. der Benutzer zu einem _Login-URL_ 4 umgeleitet.

An dieser Stelle erfolgt die Eingabe der Zugangsdaten (Anmeldename und Kennwort). Der Server prüft diese Daten und leitet die Verbindung an den ursprünglich gewünschten Dienst 4 URL = Uniform Resource Locator – sehr vereinfacht übersetzt ist dies die Internet-Adresse.

**144** 5 Benutzerverwaltung

weiter. Dabei übergibt der CAS-Server ein Token an den Webbrowser, über den die Verbindung zur Seite (z. B. die Moodle-Startseite) hergestellt wurde.

Moodle5 überprüft das Token bzw. „Ticket“ über eine weitere Adresse – den _Validation-URL_ –

beim CAS. Gibt dieser Server „grünes Licht“, wird der Zugriff auf den Dienst gewährt. Das gleiche Prinzip wird nun auch bei allen anderen Diensten verwendet, die mit dem CAS

kooperieren. Somit ist nur eine einmalige Anmeldung mit einem einzigen Satz Zugangsdaten erforderlich. Auch die Abmeldung vom System erfolgt zentral über einen _Logout-URL_.

**CAS – Protokollspezifikationen**

CAS ist ein offenes Protokoll. Die Spezifikationen sind frei zugänglich:

[_https://github.com/apereo/cas/blob/master/docs/cas-server-documen_](https://github.com/apereo/cas/blob/master/docs/cas-server-documentation/protocol/CAS-Protocol-Specif)

[_tation/protocol/CAS-Protocol-Specification.md_](https://github.com/apereo/cas/blob/master/docs/cas-server-documentation/protocol/CAS-Protocol-Specif)

■

**■**

**■ 5.2■Kennwortregeln bearbeiten**

Wer die Zugangsdaten – Anmeldename und Kennwort – kennt, kann sich mit fremder Identität in das System einloggen. Im „harmlosesten“ Fall kann diese Person sehen und lesen, welche Arbeiten und mit welchem Erfolg jemand bereits abgeliefert hat. Es ist aber auch denkbar, in dessen Namen Arbeiten zu fälschen oder zu manipulieren. Das kann weit-reichende Konsequenzen haben, deren Auswirkungen sogar den Erfolg der Lehrmaßnahme in Frage stellen können. Abgesehen davon, dass ein „schwaches Kennwort“ als grobe Fahrlässigkeit zu werten ist, was zum Ausschluss von eventuellen Haftungsansprüchen oder sogar zu einer aktiven Mitschuld im Schadensfall führen kann, sollte an dieser Stelle auch deutlich werden, dass _Identitätsdiebstahl_ durchaus strafrechtliche Konsequenzen nach sich ziehen kann.

Auch ohne Kenntnis des Kennworts kann ein Benutzerzugang sabotiert werden. Deshalb ist es möglich (und auch zu empfehlen), dass Moodle Falscheingaben erkennt und nach einer gewissen Anzahl von Fehleingaben das Konto automatisch sperrt. Im Normalfall wird man die Sperre zeitlich begrenzen, um automatischen „Passwort-Knackern“ – Fachleute sprechen von einer _Brute-Force-Attack_ – keine Chance zu geben, einfach alle möglichen Passwörter auszuprobieren. Für den legitimen In haber des Kontos ist dies natürlich eine Sicher-heitsfunktion, jedoch könnte damit auch systematisch die Nutzung des Moodle-Systems für diese Benutzerin oder diesen Benutzer blockiert werden. Derartige Denial-of-Service-Attacken lassen sich erschweren, wenn der Anmeldename nicht aus dem Klarnamen oder sonstigen Daten wie zum Beispiel einer Matrikelnummer abgeleitet werden kann.

5 _Achtung:_ Das entsprechende Plugin muss aktiviert und die Authentifizierung mit einem CAS freigegeben werden.

![Image 113](index-168_1.jpg)

![Image 114](index-168_2.jpg)

5.2 Kennwortregeln bearbeiten

**145**

**Bild 5.19** Die Kennwortregeln werden nicht im Bereich _Benutzer/innen_ bearbeitet. Sie gehören zu den _Sicherheitsregeln der Webseite!_

**Bild 5.20** Die Erhöhung der Mindestanzahl von Zeichen für das Kennwort erschwert Brute-Force-Attacken.

![Image 115](index-169_1.jpg)

**146** 5 Benutzerverwaltung

Auch wenn Kennwörter einen direkten Bezug zu Benutzerinnen und Benutzern haben, so haben sich die Entwickler der Moodle-Plattform entschlossen, die Vorgabe der Kennwortregeln in die Sicherheitsregeln der Webseite zu verlegen. Dieser Bereich ist sehr komplex.

So kann beispielsweise festgelegt werden, ob es Suchmaschinen erlaubt ist, die Seiten zu indizieren und dann in den Ergebnissen darauf zu verweisen. Das betrifft zum Beispiel auch einen „Gastzugang“ von Suchmaschinen. Auch Speichergrößen, wie zum Beispiel der Speicherplatz für die persönliche Dateiablage kann (und sollte bei begrenztem Systemspeicher-platz und hoher Auslastung) begrenzt werden. In diesem Abschnitt sollen jedoch die Kenn-wortstrukturen im Fokus stehen. Die Administration kann hier einen ganz erheblichen Beitrag zur Sicherheit des Moodle-Systems leisten.

Werden zusätzlich Umlaute und Sonderzeichen zu Ziffern und Buchstaben in Groß- und Kleinschreibung beim Anmeldenamen erlaubt, dann erweitert dies natürlich die Freiheit in der Gestaltung eines Benutzernamens, kann jedoch auch zu Problemen führen. Moodle führt hier zum Beispiel deutsche Umlaute wie ä, ö und ü an, die nicht Teil eines jeden Zeichensatzes sind. Grundsätzlich zugelassen sind Unterstrich, Punkt, Bindestrich und das Zeichen „@“. Aus diesen Gründen ist die Option in der Standardeinstellung deaktiviert.

**Auch der Anmeldename ist sicherheitsrelevant!**

Die Bedeutung des Anmeldenamens ist vielen nicht bewusst. Wer zwar nicht im Besitz des Kennworts ist, dafür aber den Anmeldenamen kennt, kann

durch gezielte mehrfache Falscheingabe einer Benutzerin bzw. einem

Benutzer für eine gewisse Zeit den Zugang zum Moodle-System verwehren!

Im Ausbildungs- und Schulbereich gehören „Streiche“ zum guten Umgangs-

ton der Lernenden! Passiert dies zu einem Prüfungstermin, kann dies mit

administrativen Unannehmlichkeiten verbunden sein.

■

**Bild 5.21** Die Festlegung der Regeln wird im System auch automatisch in den Eingabe anweisungen umgesetzt. Eine zusätzliche Änderung in den Texten ist nicht erforderlich.

![Image 116](index-170_1.jpg)

5.2 Kennwortregeln bearbeiten

**147**

Die Problematik, dass absichtliche Fehleingaben von Zugangsdaten zur Sperre eines Benutzerkontos führen können, muss Lehrenden bewusst sein. Lernende sind oft noch in einer charakterlichen Reifephase und so gehören Scherze und Streiche zum Schulalltag dazu. Auf eine Reaktion permanenter Falscheingaben zu verzichten, würde allerdings ein gravierendes Sicherheitsproblem darstellen. In diesem Fall könnten Algorithmen gezielt ausgewählte Benutzerinnen und Benutzer angreifen und durch permanentes Ausprobieren des Kennworts Zugriff auf das Konto erlangen und dessen Identität übernehmen.

In der Standardeinstellung ist die _Schwelle zur Kontosperrung_ ausgeschaltet. Ein beliebter Grenzwert sind drei Fehlversuche. Dies ist beispielsweise bei Bankkarten an Geldautoma-ten ein geläufiger Wert. Es erfüllt aber bei einem gut gewählten Kennwort auch den gewünschten Sinn, die Schwelle großzügig zu bemessen. So kann man durchaus zehn oder 20 Fehlversuche einräumen.

Neben der Höchstgrenze von maximal tolerierten Fehlversuchen können auch zeitliche Grenzwerte festgelegt werden. Mit der ersten Fehleingabe eines Passworts startet ein Kontrollzeitraum. Innerhalb dieser Zeit werden die Fehleingaben gezählt. Werden die richtigen Zugangsdaten eingegeben oder erfolgt ein weiterer Login-Versuch nach Ablauf dieses Kon trollzeitraumes, so beginnt die Zählung von Neuem. Die Standardeinstellung ist hier 30 Minuten.

**Bild 5.22** Innerhalb des Kontrollzeitraums werden die Fehlversuche bei der Anmeldung gezählt.

Erfolgt bis zum Ablauf des Kontrollzeitraums kein Anmeldefehler, wird der Zähler zurückgesetzt. Die Kontosperrdauer legt fest, nach welchem Zeitraum ein durch Fehl anmeldungen gesperrtes Konto wieder freigegeben wird.

**148** 5 Benutzerverwaltung

Die Sicherheit steigert nicht nur ein kompliziertes und langes Kennwort, sondern auch dessen Einmaligkeit. Da viele Menschen versuchen, den Lernaufwand für Kennwörter gering zu halten, neigen sie zu bereits verwendeten Kennwörtern. Dies ist ein großes Risiko, denn wenn ein solches Passwort kompromittiert wurde, könnte es durchaus in einer Art „Dictionary Attack6“ verwendet werden, um den Zugang zu knacken. Auch besteht ein Risiko, wenn andere Personen die Kennwortvorlieben eines Menschen kennen, weil das Kennwort möglicherweise auch in anderen Systemen verwendet wird.

Die Systemsicherheit und die der Benutzerin bzw. des Benutzers werden verbessert, wenn die mehrfache Verwendung eines Kennworts verhindert wird. Um die Einschränkung nicht zu sehr zu übertreiben, kann eine Anzahl für Kennwortänderungen definiert werden, nach der eine erneute Nutzung wieder möglich wird.

**Begrenzte Wirkung!**

Die Verhinderung einer erneuten Kennwortnutzung funktioniert ausschließlich bei einer lokalen Authentifizierung, weil die Hash-Werte der Kennworte ausschließlich in einer lokalen Datenbank gespeichert werden. Externe Authentifizierungsverfahren können mit dieser Einschränkung nicht belegt werden, weil die administrative Verantwortung nicht im Bereich des Moodle-Systems liegt.

■

Wird allerdings die Zahl der zulässigen Fehlversuche erreicht, geht das Moodle-System von einem Angriff auf das Benutzerkonto aus und sperrt dieses komplett. Während der Konto-sperre ist auch mit der Eingabe des korrekten Kennworts keine Anmeldung am System mehr möglich. Die Länge dieser Sperre kann von der Administration eingestellt werden.

Auch hier ist der Standardwert bei 30 Minuten voreingestellt. Es lassen sich jedoch beliebige Vorgaben im Bereich weniger Sekunden bis hin zu Wochen auswählen. Letzteres ist jedoch in der Regel nicht sinnvoll.

**Keine Information für Hacker!**

Nach mehrmaligen Falscheingaben wird auch mit den richtigen Zugangs daten keine Anmeldung am System möglich sein. Moodle wird auch in diesem Fall

grundsätzlich mitteilen, dass die Zugangsdaten falsch sind. Hier soll mit Absicht kein positives „Feedback“ an einen eventuellen Angreifer gesendet werden. Erst nach Ablauf der Sperrzeit ist eine Anmeldung wieder möglich.

■

6 Wörterbuch-Angriff – anstatt Zeichen für Zeichen beim Versuch, ein Passwort zu knacken, auszutesten, versuchen Angriffsalgorithmen existierende Wörter und Wortgruppen als Kennwort zu verwenden. Eine Variante dieser Methode ist es, bei bekannten Opfern Begriffe auszuprobieren, die einen persönlichen Bezug haben. Beispiele sind Geburtstage, Namen von Freunden und Verwandten sowie von Haustieren etc.

![Image 117](index-172_1.jpg)

![Image 118](index-172_2.jpg)

5.2 Kennwortregeln bearbeiten

**149**

**Bild 5.23** Wer merkt sich schon gerne neue Passwörter? Besonders unbeliebt ist es, für verschiedene Portale unterschiedliche Kennwörter zu haben. Dennoch ist es sicherheitstechnisch grundsätzlich zu empfehlen, mit Gewohnheiten zu brechen und individuelle Passwörter ohne „Vergangenheit“

zu erzwingen.

**Bild 5.24** Das kann schon mal passieren: Der Anmeldename oder das Kennwort wurden falsch geschrieben. Passiert dieser Fehler aber zu oft hintereinander, ist eine Anmeldung nicht mehr möglich. Aus Sicherheitsgründen wird die Benutzerin bzw. der Benutzer darüber _nicht_ in der Anmeldeseite informiert!

![Image 119](index-173_1.jpg)

**150** 5 Benutzerverwaltung

**Bild 5.25** Im Fall einer Fehleingabe sendet Moodle einen Link zum Entsperren des Benutzerzugangs. Doch Achtung: Wenn der Link direkt anklickbar ist, sollte zuvor geprüft werden, ob er auch tatsächlich zur regulären Moodle-Adresse führt!

Wenn das Moodle-Konto aufgrund von Fehleingaben gesperrt wurde, kann die Benutzerin oder der Benutzer die im System programmierte Wartezeit verkürzen. Dazu sendet Moodle automatisch eine E-Mail an die betroffene Benutzerin bzw. den betroffenen Benutzer. Diese E-Mail enthält einen Link mit einem Entsperr-Code. Die Auswahl dieses Links führt auf die Anmeldeseite, über die nun wieder – mit den richtigen Zugangsdaten – eine Anmeldung erfolgen kann.

**Den E-Mail-Text ändern?**

Der Text der E-Mail kann individuell und persönlicher gestaltet werden. Dazu muss der entsprechende Eintrag im Sprachpaket bearbeitet werden. Dieses

ist über die Moodle-Website-Administration zugänglich:

_Website-Administration – Sprache – Sprachanpassung – Filtertexte_

Hier wird in der Komponenten-Rubrik _core – admin.php_ gesucht:

_**lockoutemailbody**_

■

Es kann durchaus passieren, dass Benutzerinnen bzw. Benutzer des Systems die Abwei-sung der Anmeldung nicht verstehen. Besonders dann nicht, wenn sie sich – nach Über-schreiten der maximalen Anzahl der Login-Versuche – „sicher sind“, die richtigen Zugangsdaten eingegeben zu haben. Hier kann die Administration Aufklärung liefern. Die Moodle-Systemverwalterin bzw. der Systemverwalter können das betreffende Benutzerprofil einsehen. Dies ist in der Website-Aministration im Abschnitt _Nutzer/innen_ – _Nutzerkonten_ in den _Benutzerlisten_ (vgl. Abschnitt 5.4) möglich. Hier lassen sich gezielt Profile aufrufen.

![Image 120](index-174_1.jpg)

5.3 Benutzerprofile

**151**

Die Administration hat eine erweiterte Ansicht des Dashboards und kann vielseitige Berichte einsehen. Dies betrifft auch die sogenannten „ _Log-Daten_“. Hier sind alle von der betreffenden Benutzerin bzw. dem Benutzer verursachten Ereignisse aufgelistet. Das betrifft auch Fehlversuche bei der Anmeldung (Error ID ΄3΄) und Sperrzeiten nach wiederholter Fehleingabe (Error ID ΄4΄). In Bild 5.26 ist ein solcher Fall dokumentiert. Für betroffene Benutzerinnen bzw. Benutzer gilt die Empfehlung, das E-Mail-Postfach zu prüfen und den Entsperr-Code zu aktivieren bzw. die Sperrzeit abzuwarten.

**Bild 5.26** Die Administration kann in den Profilen der jeweiligen Benutzerinnen und Benutzer erkennen, ob fehlerhafte Zugangsversuche und infolge dessen eine Sperre erfolgten.

**■**

**■ 5.3■Benutzerprofile**

Moodle ist eine Lernplattform, jedoch stellt diese Plattform innerhalb des Systems auch ein soziales Netzwerk dar, über das Lernende und Lehrende sich kennen lernen und über verschiedene Foren und über Nachrichten austauschen können. Damit trägt Moodle innerhalb einer in sich geschlossenen IT-Umgebung zu einer sicheren Kommunikation bei. Das Moodle- System ist hier eine vertrauenswürdige Umgebung, welche sich an die geltenden Gesetze zum Datenschutz zu halten hat.

Jede einzelne Benutzerin und jeder einzelne Benutzer ist Teil dieser Community und beschreibt sich selbst durch ein eigenes Profil. Dieses besteht aus verschiedenen Arten von Feldern:

**152** 5 Benutzerverwaltung

**Pflichtfelder:** Diese sind Vor- und Nachname sowie die E-Mail-Adresse. Diese Felder müssen ausgefüllt werden, wobei jedoch die E-Mail-Adresse auf Wunsch der Benutzerin bzw. des Benutzers bei der Ansicht der Profile verborgen werden kann.

**Freiwillige Eingaben:** Hierzu gehören Stadt, Land, eine Beschreibung etc. Es obliegt der Benutzerin oder dem Benutzer, diese Felder mit Eingaben zu füllen oder diese Angaben nicht in Moodle zu veröffentlichen. Dies gilt auch für ein Nutzerbild.

Darüber hinaus ist das Profil der Benutzerinnen und Benutzer in verschiedene Bereiche aufgeteilt:

Allgemeines

Nutzerbild

Weitere Namen

Persönliche Interessen

Optionale Einträge

Diese Bereiche sind die sogenannten _Standard-Profilfelder_. Sie sind bereits mit der Moodle-Installation eingerichtet. Ohne weitere Veränderung in den Definitionen lassen sich mit deren Hilfe bereits aussagekräftige Profile gestalten. Der Umfang der Standardfelder der Profile ist von der Administration nicht zu verändern. Das gilt auch für die Pflichtfelder.

Zusätzlich können _weitere Profilfelder_ mit unterschiedlichen Eigenschaften definiert werden, die über den allgemeinen Standard hinausgehen.

**Abweichung vom Standard**

Bei der Verwendung „weiterer Profilfelder“ müssen am System arbeitende

Kollegen auf diese Felder hingewiesen werden. In anderen Installationen

sind diese Felder, deren Definition und deren Bedeutung unbekannt!

■

**5.3.1■Standard-Profilfelder**

Die in Moodle definierten Standard-Profilfelder können nicht aus dem System gelöscht werden. Darüber hinaus ist es möglich, die Veränderbarkeit einzelner Felder einzuschränken.

Das ist beispielsweise bei den Realnamen sinnvoll, um Zuordnungspannen bei nicht elektronischen Bewertungen durch die Schuladministration zu verhindern.

Bei den Einschränkungen sind drei Optionen vorgesehen:

_Bearbeitbar_ – Benutzerinnen und Benutzer können das Feld ihres eigenen Profils frei bearbeiten und jederzeit den Inhalt des Felds verändern.

_Bearbeitbar (wenn leer)_ – Benutzerinnen und Benutzer können das Feld ihres eigenen Profils nur dann bearbeiten, wenn es noch leer ist. Bestehende Einträge sind nicht mehr zu verändern und fordern den Kontakt mit der Administration.

_Gesperrt_ – Felder, die mit dieser Einstellung belegt sind, können ausschließlich durch die Administration gefüllt und bearbeitet werden.

![Image 121](index-176_1.jpg)

![Image 122](index-176_2.jpg)

5.3 Benutzerprofile

**153**

**Bild 5.27** Ein gesperrtes Profilfeld kann von der Benutzerin bzw. dem Benutzer nicht geändert werden.

**Bild 5.28** Ein frei beschreibbares Feld bietet die Möglichkeit, etwas über die eigene Person zu schreiben, was in keinem Feld abgefragt wird. In einer Lehrplattform ist es sinnvoll, hier etwas über die belegten Fächer und Kurse zu hinterlassen.

Die Einschränkung der Änderungsmöglichkeiten erfolgt in der _Website-Administration_ im Abschnitt _Plugins_/ _Authentifizierung_/ _Manuelle Konten_. Eine Sperre der Veränderungsmög-lichkeiten ist für die Felder sinnvoll, die ausschließlich durch die Administration bearbeitet und an die allgemeinen Personal- und Studierenden akten angepasst werden. Dies kann beispielsweise Referenzen zur Personal- oder Matrikelnummer betreffen.

**154** 5 Benutzerverwaltung

Insbesondere ist dies beim sogenannten Bulk-Upload, also beim Hochladen gleich mehrerer Profile von Benutzerinnen und Benutzern aus einem externen Datenbestand in Form einer CSV7-Datei sinnvoll. Das gewährleistet die Kompatibilität von Moodle zu den externen Datenbeständen und erleichtert es Benutzerinnen und Benutzern aus der allgemeinen Verwaltung heraus in das Moodle-System zu inte grieren. Zu den Details dieses Verfahrens vgl.

Abschnitt 5.3.3.

Ein oft unterschätztes und doch nützliches Standardfeld ist die „Beschreibung“. An dieser Stelle können jede Benutzerin und jeder Benutzer etwas zur eigenen Person vermerken. Da es sich um eine Lernplattform handelt, bietet es sich an, etwas über fachliche Interessen in das Profil zu schreiben. So können sich Lernende untereinander austauschen und individuelle Lerngruppen bilden. Ähnlich sieht es aber für Lehrende aus, die mit diesem Feld die Möglichkeit haben, individuelle Mitteilungen (z. B. persönliche Sprechstunden, Angebote für Abschlussarbeiten, spezia li sierte Fachgebiete etc.) zu deponieren.

**Bearbeitungsrechte festlegen**

Ob eine Benutzerin oder ein Benutzer einzelne Felder bearbeiten darf oder nicht, wird in den Einstellungen der Authentifizierungs-Plugins für _Manuelle_ _Konten_ festgelegt:

_Website-Administration – Plugins – Authentifizierung – Manuelle Konten_

■

**5.3.2■Weitere Profilfelder**

Neben den Standard-Profilfeldern können weitere Felder für das Profil vorgesehen werden.

Diese Felder sind selbstverständlich nur Bestandteil der Profile in dieser einen Lernplattform. Das muss beachtet werden, wenn einmal Lernplattformen zusammengeführt oder in andere Systeme übernommen werden.

**Festlegung weiterer Profilfelder**

Die Festlegung weiterer Profilfelder erfolgt im Bereich _Nutzer/innen_ in der Website-Administration:

_Website-Administration – Nutzer/innen – Profilfelder_

■

Weitere Profilfelder können in verschiedenen Arten definiert werden:

Datum- und/oder Zeitfeld

Dropdown-Menü

Markierungsfeld

7 CSV steht für Comma Separated Values – durch Kommata getrennte Werte. Es handelt sich um eine reine Textdatei. In der ersten Zeile werden – durch Kommata getrennt – die Spaltenüberschriften (Felder im Datensatz) und in den weiteren Zeilen – ebenfalls durch Kommata getrennt – die Werte der einzelnen Datensätze geschrieben.

![Image 123](index-178_1.jpg)

![Image 124](index-178_2.jpg)

5.3 Benutzerprofile

**155**

Textbereich

Texteingabe

**Bild 5.29** Das Profil kann um verschiedene weitere Profilkategorien und darin um weitere Datenfelder ergänzt werden.

**Bild 5.30** Den „weiteren Profilkategorien“ kann jeweils ein individueller Name zugewiesen werden.

Es lassen sich verschiedene Profilkategorien anlegen und innerhalb dieser Kategorien verschiedene Datenfelder einrichten. Jedes Datenfeld kann mit individuellen Eigenschaften versehen werden. Das betrifft zum Beispiel die Sichtbarkeit des Felds (grundsätzlich sichtbar für alle, nicht sichtbar oder nur für Teilnehmer/innen sichtbar).

![Image 125](index-179_1.jpg)

![Image 126](index-179_2.jpg)

**156** 5 Benutzerverwaltung

**Bild 5.31** Für jedes ergänzende Profilfeld können Regeln festgelegt werden. Unter anderen kann die Sichtbarkeit des Felds auf bestimmte Benutzergruppen eingeschränkt werden.

**Bild 5.32** Für die Definition eines Drop-down-Menüs werden die Menüeinträge zeilenweise in das Optionsfeld eingetragen.

![Image 127](index-180_1.jpg)

5.3 Benutzerprofile

**157**

**Bild 5.33** Im Profil erscheint nun das neue Feld in der festgelegten Kategorie mit den gewählten Eigenschaften.

**5.3.3■Benutzerprofile per Bulk-Upload einrichten**

Sollen mehrere Benutzerinnen und Benutzer gemeinsam in das System aufgenommen werden, stellt dies über die gängigen Webformulare einen großen Arbeits- und Zeitaufwand dar.

Wenn die Basisdaten wie Namen und E-Mail-Adressen bereits in einer anderen Datei vorliegen und damit bekannt sind, können sie in eine CSV-Datei – CSV steht für Comma Separated Values – exportiert werden.

Eine CSV-Datei kann beispielsweise aus Datenbanken oder aus einer Excel-Datei ex portiert werden. Der Begriff „durch Kommata getrennt“ ist allerdings nicht zu ge nau zu nehmen, denn als Trennzeichen können auch andere Zeichen verwendet werden:

Komma (,)

Semikolon (;)

Doppelpunkt (:)

Tabulator (\t)

Eine Benutzerdatei, die alle Pflichtelemente (Benutzername, Vorname, Name, E-Mail-Adresse) enthält, zeigt das folgende Listing:

username,firstname,lastname,email

student4,Student 4,Bulkupload,moodle.student4@srg.at

student5,Student 5,Bulkupload,moodle.student5@srg.at

teacher3,Teacher 3,Bulkupload,moodle.teacher3@srg.at

Die Datei wird im UTF-8-Format gespeichert. Wenn ein anderer Zeichensatz gewählt wird, muss dieser auf jedem Fall beim Upload im Feld _Encoding_ richtig eingestellt werden. Sonst kann Moodle die Informationen nicht richtig zuordnen. Als Trennzeichen wurde hier das

**158** 5 Benutzerverwaltung

Komma gewählt. In Deutschland und in Österreich sind allerdings auch das Semikolon oder der Tabulator sehr gebräuchlich. Dies kann also frei festgelegt werden.

Für die Moodle-Profilfelder gibt es folgende Spaltenbezeichnungen

username,

email,

firstname,

lastname,

idnumber,

institution,

department,

phone1,

phone2,

city,

url,

icq,

skype,

aim,

yahoo,

msn,

country

In einer CSV-Datei können auch zusätzlich deklarierte Profilfelder berücksichtigt werden.

Beispiele sollen die zuvor deklarierten „weiteren Profilfelder“ sein. Zur Erinnerung: Für den Namen des Felds wurden eine eindeutige Kurzbezeichnung und ein erklärender Name definiert. Die Kurzbezeichnung ist die interne Bezeichnung des Felds, wie sie auch als Teil der Spaltenbeschriftung in der CSV-Datei verwendet wird. Eingeleitet werden die Spaltennamen für die weiteren Profilfelder mit _profile_field__.

Die im Beispiel erzeugten neuen Profilfelder haben die Kurzbezeichnungen „Fachgebiete“

und „Themenangebote“. Damit setzen sich die CSV-Spalten für diese beiden Profilfelder wie folgt zusammen:

profile_field_Fachgebiete

profile_field_Themenangebote

**Wie heißen die Profilfelder im eigenen Moodle-System?**

Es ist möglich, die im Moodle-System gespeicherten Profile als CSV-Datei zu exportieren. Auch diese Datei wird in ihrer ersten Zeile die Spaltenüberschriften enthalten, die für den Upload von Benutzerprofilen verwendet werden können.

Ausführlich beschreibt Abschnitt 5.4.3 den Download der Profile.

■

![Image 128](index-182_1.jpg)

5.3 Benutzerprofile

**159**

**Bild 5.34** Beim Hochladen einer Benutzerdatei im CSV-Format muss sichergestellt sein, dass sowohl der Zeichensatz als auch das in der Datei verwendete Trennzeichen den Einstellungen entsprechen.

Moodle liest die Daten Zeile für Zeile aus und ordnet die Informationen den jeweiligen internen Feldern zu. Diese sind in der CSV-Datei in der ersten Zeile deklariert.

Mit dem Hochladen der Datei allein ist der Vorgang jedoch noch nicht abgeschlossen, denn es können Benutzerinnen oder Benutzer bereits vorhanden sein. Es muss also festgelegt werden, wie mit Duplikaten umzugehen ist. Natürlich müssen auch die neuen Benutzerinnen und Benutzer eigene Zugangsdaten mit einem sicheren Kennwort haben. Diese Kennwörter werden in Moodle automatisch erzeugt. Sie werden also nicht mit der CSV-Datei hochgeladen, weil dies ein Sicherheitsproblem darstellen würde. Stattdessen wird den neuen Benutzerinnen und Benutzern ein Zufallskennwort per E-Mail zugeschickt, welches diese bei der ersten Anmeldung individuell ändern müssen.

**Authentifizierung neuer Benutzerinnen und Benutzer**

Es ist zu empfehlen, Benutzerinnen und Benutzern ein automatisch generiertes Kennwort per E-Mail zuzusenden, was zwangsweise bei der ersten Anmeldung zu ändern ist. Auf diese Weise wird ein hohes Maß an individueller Sicherheit erreicht.

■

![Image 129](index-183_1.jpg)

**160** 5 Benutzerverwaltung

Natürlich muss der Datenschutz der neu angelegten Benutzerinnen und Benutzer beachtet und respektiert werden. Man kann die Ansicht der E-Mail-Adresse grundsätzlich oder nur für Kursteilnehmer sichtbar machen oder unterbinden. Im letz teren Fall haben nur administrative Mitglieder des Systems Zugriff auf diese In formation.

**Bild 5.35** Wenn die CSV-Datei in das System geladen wurde, muss festgelegt werden, wie mit bereits vorhandenen Benutzern verfahren werden soll und wie ein neues Kennwort erzeugt wird.

![Image 130](index-184_1.jpg)

![Image 131](index-184_2.jpg)

5.3 Benutzerprofile

**161**

**Bild 5.36** Es wird nicht nur festgelegt, ob ein Kennwort erzeugt und per E-Mail an die Benutzerin bzw. den Benutzer verschickt wird. Auch die Anzeige der E-Mail-Adresse kann eingeschränkt werden.

**Bild 5.37** Das Ergebnis des Bulk-Uploads wird statistisch angezeigt. Hier kann die Administration überprüfen, ob wirklich alle Profile angelegt wurden.

![Image 132](index-185_1.jpg)

**162** 5 Benutzerverwaltung

**■**

**■ 5.4■Benutzerlisten**

Ob die neuen Benutzerinnen und Benutzer im System „angekommen“ sind und ob sie bereits aktiv waren, lässt sich durch einen Blick in die _Benutzerlisten_ feststellen. Die Benutzerliste ist ein sehr wichtiges Werkzeug für die Administration. Hiermit lässt sich feststellen, wann welche Benutzerin und welcher Benutzer zuletzt online waren und ob diese Personen überhaupt Moodle nutzen. In Bild 5.38 wird ersichtlich, dass die im letzten Abschnitt neu angelegten Benutzerinnen und Benutzer sich noch nie im System angemeldet haben.

Diese Benutzerliste ist der Abschluss des Bulk-Uploads. Sie lässt sich aber auch über die Website-Administration aufrufen. Im Register _Nutzer/innen_ ist der Link auf die Benutzerlisten gleich ganz oben im Abschnitt _Nutzerkonten_ zu finden.

Die einzelnen Profile lassen sich von der Administration gezielt bearbeiten, was beispielsweise wichtig ist, wenn eine Benutzerin oder ein Benutzer das Zugangskennwort vergessen hat. Die Administration kann allerdings auch Benutzer vorübergehend sperren oder vollständig aus dem System entfernen.

**Bild 5.38** In der Benutzerliste hat die Administration Zugriff auf alle im System registrierten Benutzerprofile und kann einzelne Profile vorübergehend deaktivieren oder vollständig löschen.

**5.4.1■Nach Benutzerin oder Benutzer suchen**

In diesem Testsystem sind gerade einmal acht Benutzerinnen und Benutzer registriert.

Natürlich werden Moodle-Systeme in der Praxis weitaus mehr Benutzerinnen und Benutzer umfassen. In Schulen existieren schnell mehrere hundert, in Universitäten sogar mehrere tausend Personen im System, die einen aktiven Zugang besitzen. Hier gibt es einen Interes-senskonflikt, denn viele Benutzerprofile bremsen das System. Auf der anderen Seite muss Absolventen auch die Möglichkeit gegeben werden, über einen gewissen Zeitraum auf die eigenen Arbeitsleistungen zugreifen zu können. Möglicherweise ist auch aus rechtlicher

![Image 133](index-186_1.png)

5.4 Benutzerlisten

**163**

Sicht eine Dokumentationspflicht gegeben. Der Umfang der Benutzerliste kann also schnell sehr große Ausmaße erreichen.

Die Benutzerliste bietet einige Möglichkeiten, den Umfang der Darstellung einzugrenzen.

So kann beispielsweise gezielt nach der E-Mail-Adresse oder Teilen davon gesucht werden.

Auch kann die Sortierung der Liste verändert werden: Ein Klick auf die Spaltennamen sorgt für eine Aufwärts- oder Abwärtssortierung in der betreffenden Spalte.

**Bild 5.39** Die Administration weist einem – in der Benutzerliste ausgewählten – Benutzer ein neues Kennwort zu. Aus Sicherheitsgründen wird eine Änderung des Kennworts bei der ersten nun folgenden Anmeldung erzwungen.

**5.4.2■Nach anderen Kriterien suchen**

In Bild 5.38 ist unter „Neue Suche“ ein Drop-down-Menü „E-Mail-Adresse enthält“ zu sehen.

E-Mail-Adressen können bei beliebigen Anbietern bezogen und mit Phantasienamen gestaltet werden. Sie sind also ein denkbar schlechtes Suchkriterium in einem hochkomplexen System. Ein anderes, möglicherweise sinnvolleres Suchkriterium muss an anderer Stelle im Bereich _Nutzerkonten – Nutzerverwaltung_ eingestellt werden.

Es können gezielte Vorgaben für das Suchkriterium gemacht werden, wobei diese Kriterien nicht alleine auf die Profilfelder beschränkt sind. Interessant sind die Daten, welche die Nutzung zwangsweise begleiten wie die exakten Zugangszeiten in das System oder die dabei verwendete IP-Adresse. IP-Adressen sind gewissermaßen die Visitenkarte bei jeder Bewegung im Internet. Wird beispielsweise ein Zugang gehackt und missbraucht und sind hierbei sowohl die IP-Adresse als auch die Uhrzeit und das Datum bekannt, können sehr eindeutige Rückschlüsse auf den Anschlussinhaber und damit zu einer Person gemacht werden. Es gibt also eine begründete Chance, Störer im System zu ermitteln.

![Image 134](index-187_1.jpg)

**164** 5 Benutzerverwaltung

**IP-Adressen sind wie Personalausweise – oder?**

Eine ungefälschte IP-Adresse kann tatsächlich – einer persönlichen Visitenkarte vergleichbar – mit einer physischen Person in Verbindung gebracht werden, wenn dies legitimierte Ermittlungsbehörden veranlassen. Allerdings gibt es auch Netzwerke wie TOR8, die Internet-Verbindungen über verschiedene Knotenpunkte mit ständig wechselnden IP-Adressen herstellen. Hier wird es schwierig, IP-Adressen zu personalisieren.

■

Im Fall eines Missbrauchs im System können Recherchen in den Nutzerprofilen durchaus auch zur Entlastung der registrierten Benutzerinnen und Benutzer beitragen. Identitätsdiebstahl ist ein weit verbreitetes Problem in digitalen Systemen. Angreifer erlangen hier oft durch Phishing Kenntnis von den Zugangsdaten ihrer Opfer. Die Auswertung dieser Daten eignet sich zudem zum Nachweis von Betrugsversuchen bei digitalen Prüfungen im Moodle-System.

**Bild 5.40** Für die Suche in der Nutzerliste muss ein Suchkriterium voreingestellt werden. Hierzu kommen alle Standard-Profilfelder, aber auch dynamische Daten wie zum Beispiel die verwendete IP-Adresse oder der letzte Zugriff etc. in Betracht.

8 TOR steht als Abkürzung für „The Onion Routing“. Es bezeichnet das Prinzip des mehrschichtigen Datentransports über das Anonymisierungsnetzwerk [_www.torproject.org._](http://www.torproject.org)

![Image 135](index-188_1.jpg)

5.4 Benutzerlisten

**165**

**Bild 5.41** Hier wird nach Teilen einer zuletzt für den Zugriff verwendeten IP-Adresse gesucht. Damit können beispielsweise Störer ausfindig gemacht werden.

**5.4.3■Benutzerverwaltung (Bulk)**

Im Bereich _Website-Administration – Nutzer/innen – Nutzerkonten_ findet man den Eintrag _Benutzerverwaltung (Bulk)_. In diesem Bereich können aus den mit dem Filterkriterium gefundenen Benutzerinnen und Benutzern gezielt Personen selektiert werden. Mit diesen Moodle-Teilnehmerinnen und -Teilnehmern können nun (blockweise) gemeinsame Aktionen durchgeführt werden:

Bestätigen der Mitgliedschaft im System.

Löschen aus dem System.

Versenden einer E-Mail.

Aufforderung zu einer Kennwortänderung.

Anzeige auf einer Seite.

Hinzufügen zu einer globalen Gruppe.

**Hinweis:**

Für dieses Beispiel wurde in der _Nutzerverwaltung_ (Abschnitt 5.4.2 ) der _Standardmäßige Nutzerfilter_ auf _Anmeldename_ gesetzt.

■

![Image 136](index-189_1.jpg)

![Image 137](index-189_2.jpg)

**166** 5 Benutzerverwaltung

**Bild 5.42** Hier wurden alle Benutzerinnen und Benutzer des Moodle-Systems gesucht, deren An -

meldename „student“ enthält.

**Bild 5.43** Es können gezielt einzelne Benutzerinnen bzw. Benutzer selektiert oder die gesamte Trefferliste für weitere Operationen übernommen werden.

Die Bulk-Suche gestattet es der Administration, gezielt Benutzerinnen oder Benutzer nach bestimmten Kriterien zu suchen. Damit lässt sich in einer möglicherweise sehr umfassen-den Teilnehmermenge Übersicht gewinnen.

![Image 138](index-190_1.jpg)

5.5 Globale Gruppen

**167**

**■**

**■ 5.5■Globale Gruppen**

Während _Gruppen in Kursen_ vom „Teacher“, also von der Lehrerin bzw. dem Lehrer angelegt und verwaltet werden, können _globale Gruppen_ nur von der Administration eingerichtet und verwaltet werden. Für die Teacher stellen diese globalen Gruppen eine Arbeitserleichterung dar, denn sie müssen sich nicht um die Aufnahme der Lernenden in ihre Kurse kümmern.

In einer globalen Gruppe können beispielsweise die Schülerinnen und Schüler einer Klasse pro Jahrgang oder Studierende aufgenommen werden, die sich in einen bestimmten Kurs eingeschrieben haben.

**Anlegen globaler Gruppen erfordert spezielle Rechte!**

Um globale Gruppen anzulegen, sind administrative Rechte erforderlich. Diese können allerdings auch auf andere Rollen delegiert werden. Es sollte jedoch das Recht, globale Gruppen zu definieren, an zentralen Stellen des Systems verbleiben, um Chaos in der Organisation des Systems zu verhindern.

■

**5.5.1■Globale Gruppen anlegen**

Eine globale Gruppe richtet die Administration in der _Website-Administration_ im Bereich _Nutzer/innen_ bei den _Nutzerkonten_ ein. Im folgenden Beispiel wird eine globale Gruppe für das _Kernsystem_ eingerichtet. Sie soll den Namen „Teachergruppe“ und die globale Gruppen-ID „teacher1“bekommen. Der Zweck soll die vereinfachte Organisation interner Fortbildungen des eigenen Personals sein.

Es lassen sich gezielt Gruppen, beispielsweise für Klassenverbände oder Semestergruppen bilden, wodurch die Zuordnung der Benutzerinnen und Benutzer des Moodle-Systems zu einzelnen Kursen oder Lernplänen erleichtert wird.

**Bild 5.44** Es wird eine neue globale Gruppe angelegt, die Gültigkeit im Kernsystem hat.

![Image 139](index-191_1.jpg)

**168** 5 Benutzerverwaltung

**Bild 5.45** Globale Gruppen können jederzeit durch die Administration bearbeitet, ergänzt oder gelöscht werden.

**5.5.2■Globale Gruppen als CSV-Datei importieren**

Während sich einzelne _globale Gruppen_ durchaus über die _Website-Administration_ im _Nutzer/innen_-Bereich unter _Nutzerkonten_ einrichten lassen, werden mehrere globale Gruppen zweckmäßigerweise mit einer CSV-Datei gemeinsam deklariert und durch Hochladen in das Moodle-System eingerichtet.

Das ist beispielsweise dann sinnvoll, wenn ein neues Semester oder ein Schuljahr beginnt und viele Schülerinnen und Schüler neuen Klassenverbänden zugewiesen werden müssen.

Zuerst werden in diesem Fall die neuen globalen Gruppen eingerichtet und anschließend die Benutzer und Benutzerinnen in diese Gruppen aufgenommen.

name;idnumber;description

Klasse 11a-SS2020;11a-SS2020;Mathematik-Leistungskurs

Die CSV-Datei kann mit folgenden Spalten gebildet werden:

_name_: Name der neuen Gruppe. Diese soll im Beispiel Klasse11a-SS2020 für das Sommer-semester 2020 lauten. Der Name ist das einzige Pflichtelement in der CSV-Datei.

_idnumber_ (optional): Hier muss es sich nicht notwendigerweise um eine Zahl handeln. Es kann auch ein aussagekräftiges Kürzel gewählt werden.

_contextid_ (optional): Ist eine Kontext-ID eines bestimmten Kursbereichs bekannt, so kann diese hier zur Zuweisung der globalen Gruppe zu diesem Bereich verwendet werden.

_visible_ (optional): Wenn die Gruppe sichtbar ist, wird dieser Spalte der Wert „1“ zugeordnet. Sonst wird hier „0“ gesetzt.

_context_ (zusätzliche Spalte)

_category_ (zusätzliche Spalte)

_category_id_ (zusätzliche Spalte)

_category_idnumber_ (zusätzliche Spalte)

_category_path_ (zusätzliche Spalte)

![Image 140](index-192_1.jpg)

5.5 Globale Gruppen

**169**

Um die Begriffe _context_ und _category_ zu verstehen, muss man sich die interne Organisation von Moodle vor Augen führen. Das gesamte System ist hierarchisch organisiert. Ein Kontext ist ein Bezug zu einem Bereich innerhalb des Moodle-Systems, in den Benutzerinnen und Benutzern _Rollen_ zugewiesen werden können. Diese Bereiche können in Kategorien ge -

gliedert werden.

Standardkontexte in Moodle sind:

Kernsystem

Nutzer

Kursbereich

Kurs

Aktivitäten

Block

Das Kernsystem ist der Standardkontext, dem jede Gruppe zugeordnet wird, wenn keine spezielle Deklaration vorgenommen wird. Die zusätzlichen Spalten beziehen sich also auf Kontexte und Kategorien, die innerhalb des Moodle-Systems existieren müssen. Ist dies nicht der Fall, antwortet die Vorschau mit einer entsprechenden Warnmeldung.

Eine andere CSV-Datei verursacht Probleme. Es wird ein Kontext in der Deklaration beschrieben, der jedoch nicht im Moodle-System definiert wurde. Das führt zu einer Warnung, verhindert jedoch nicht die Einrichtung der globalen Gruppe. Es ist dabei zu beachten, dass die globale Gruppe mit Bezug auf den Standard kontext – Kernsystem – eingerichtet wird (Bild 5.49).

name;idnumber;description; _context_

Seminar 01;S1-2020;Fortbildung Moodle-Kursgestaltung; _interne Fortbildung_ **Bild 5.46** 

Die CSV-Datei wird

über den Standard-

Upload-Dialog von

Moodle hochgeladen.

![Image 141](index-193_1.jpg)

![Image 142](index-193_2.jpg)

**170** 5 Benutzerverwaltung

**Bild 5.47** Wichtig für den erfolgreichen Upload der globalen Gruppendefinitionen ist die Über-einstimmung von Kodierung und Trennzeichen.

**Bild 5.48** In der Vorschau kann überprüft werden, ob die globalen Gruppen korrekt definiert wurden. Erst danach erfolgen das eigentliche Hochladen und Installieren der Definitionen.

![Image 143](index-194_1.jpg)

![Image 144](index-194_2.jpg)

5.5 Globale Gruppen

**171**

**Bild 5.49** In der CSV-Datei wurde ein nicht existierender Kontext eingetragen. Die Gruppe kann mit dem Standardkontext eingerichtet werden.

**Bild 5.50** Die neue globale Gruppe taucht in der Liste nun neben der manuell angelegten Gruppe auf.

**172** 5 Benutzerverwaltung

**Bitte beachten beim Erstellen der CSV-Datei**

Die Spalten und die jeweiligen Daten müssen durch Trennzeichen (Komma,

Semikolon etc.) separiert werden. Ein leeres Datum wird durch zwei direkt nebeneinander liegende Trennzeichen dargestellt. Die Zahl der Daten muss der Anzahl der Spalten entsprechen. Der Zeichensatz der Datei (z. B. UTF-8) muss passend in Moodle gewählt werden.

■

