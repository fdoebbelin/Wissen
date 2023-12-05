Mit Stable Diffusion ist ein KI-System frei verfügbar, das eindrucksvolle Bilder erzeugt. Organisationen wie LAION und EleutherAI tragen das Non-Profit-Projekt.

![Stable Diffusion Launch Announcement, Stability AI](media/Stable_Diffusion_Launch_Announcement,_Stability_AI.jpg)

Die Familie der KI-Bildgeneratoren bekommt erneut Zuwachs, diesmal aus der Open-Source-Ecke: Mit Stable Diffusion ist ein neuronales Text-zu-Bild-Modell erschienen, das womöglich das Zeug hätte, dem bisherigen Platzhirsch [DALL·E 2 von OpenAI](https://www.heise.de/hintergrund/KI-System-DALL-E-Ein-Alleskoenner-fuer-Kreative-7206468.html) (erschienen im April 2022) und [Imagen von Google Brain](https://www.heise.de/news/Fotorealistische-KI-Bildsynthese-Google-macht-DALL-E-2-Konkurrenz-mit-Imagen-7121826.html) (vorgestellt im Mai, bislang ohne Demo) den Rang abzulaufen. Das liegt nicht nur an der hochwertigen Qualität der Bilder, sondern an der Zugänglichkeit: Durch den gemeinnützigen Ansatz der Herausgeber steht das Stable-Diffusion-Modell samt damit erzeugtem Output der Allgemeinheit frei zur Verfügung.

Nach einem geschlossenen Release Anfang August über ein Anmeldeformular (für Forscherinnen und Forscher) hat das Stable-Diffusion-Team das Modell nun für alle geöffnet. Laut Releasemeldung diente die Zeitspanne ab dem Forschungsrelease offenbar dazu, verbliebene rechtliche, ethische und technische Fragen zu klären. So enthält das Public Release einen KI-basierten Safety Classifier, der vom User unerwünschten Output entfernt. Die Parameter des Sicherheitsgurts lassen sich offenbar benutzerdefiniert einstellen.

### Frei verfügbar, kommerzielle Nutzung erlaubt

Das Modell steht unter der Lizenz "[Creative ML OpenRAIL-M](https://huggingface.co/spaces/CompVis/stable-diffusion-license)", deren Details auf Hugging Face einsehbar sind. Die Voraussetzung zum Nutzen des Modells ist das Akzeptieren dieser Lizenz, anschließend lassen die Weights sich herunterladen. Der Einsatz ist nicht auf den Privatgebrauch beschränkt, sondern auch die kommerzielle Nutzung oder das Anbieten von Diensten mit Stable Diffusion ist ausdrücklich erlaubt, sofern die lizenzbedingten Einschränkungen gewahrt werden (illegaler oder schädlicher Output sowie Content sind untersagt). Im Gegenzug tragen die Nutzer selbst volle Verantwortung für den Einsatz.

Zahlreiche User testen das System bereits ausgiebig, insbesondere in der Kombination mit Midjourney (Beta), und teilen im Internet teils eindrucksvolle Ergebnisse. In der Testphase hatten über 10.000 Betatester das Modell in Betrieb und produzierten rund 1,7 Millionen Bilder pro Tag.

The recent update to the Midjourney beta with Stable Diffusion is pretty impressive, and arguably has the edge over DALL-E 2 for the generation of striking imagery - even though it's more stylistically opinionated. https://t.co/ul0VXDWFXX

[![](media/0.jpg)](https://api.heise.de/svc/embetty/tweet/1562480868186521601/images/0)[![](media/1.png)](https://api.heise.de/svc/embetty/tweet/1562480868186521601/images/1)[![](media/2.jpg)](https://api.heise.de/svc/embetty/tweet/1562480868186521601/images/2)[![](media/3.jpg)](https://api.heise.de/svc/embetty/tweet/1562480868186521601/images/3)
### Suchmaschine Lexica erschließt Bilder und Prompts

Einsteiger können mit der [Suchmaschine Lexica die bislang mit Stable Diffusion erzeugten Bilder und Text-Prompts](https://lexica.art/) durchstöbern. Lexica erschließt derzeit über fünf Millionen Einträge, laufend werden es mehr. Wer mit Stable Diffusion oder einem anderen Text-zu-Bild-System KI-basiert Bilder erstellt, findet hier kreative Inspiration, aber auch Denkanstöße für die Forschung.

## Stable Diffusion: Bilder und Prompts finden mit Lexica

![Mines of moria, khazad dum, halls of durin, middle earth, tolkien, a bright orb of light in the center of a grand hall, outer edges shrouded in darkness with creatures crawling out into the light, in the style of hieronymus bosch](media/Mines_of_moria,_khazad_dum,_halls_of_durin,_middle_earth,_tolkien,_a_bright_orb_of_light_in_the_cent.jpg)

### Mittelerde: Minen von Moria und Khazad Dum

"Mines of moria, khazad dum, halls of durin, middle earth, tolkien, a bright orb of light in the center of a grand hall, outer edges shrouded in darkness with creatures crawling out into the light, in the style of hieronymus bosch"

Zum Training nutzte das Stable-Diffusion-Team einen Bilddatensatz aus der frei zugänglichen LAION-5B-Datenbank, die rund 5,85 Milliarden CLIP-gefilterter Bild-Text-Paare enthält und damit vierzehnmal größer ist als ihre Vorgängerin LAION-400M. LAION-Datensätze sind als Indizes für das Internet zu verstehen: Sie listen die URLs zu den Originalbildern gemeinsam mit den verknüpften ALT-Texten auf. Bis Anfang August 2022 war LAION-400M die weltweit größte öffentlich zugängliche Bild-Text-Datenbank gewesen, und zahlreiche Machine-Learning-Projekte beruhen auf Datensätzen aus dieser Quelle.

CLIP steht für Contrastive Language-Image Pre-Training und ist eine von OpenAI entwickelte Technik, die auch bei DALL·E 2 zum Einsatz kommt und visuelle Konzepte in Kategorien umsetzt. Neben eigener Arbeit (vorwiegend durch die Teams von CompVis und Runway ML) haben die Forscher sich an den Arbeiten zu DALL·E 2 (von OpenAI), Imagen (von Google Brain) und den Beiträgen der [KI-Entwicklerin Katherine Crowson](https://twitter.com/RiversHaveWings) orientiert.

### Wie funktioniert Stable Diffusion?

Eine "stabile Diffusion" läuft in zwei Schritten ab: Der Encoder komprimiert ein Bild (x) zu einer niedrigdimensionalen Darstellung (z) im latenten Raum. Anschließend laufen Diffusion und Rauschunterdrückung (Denoising), und zwar vorwiegend über die Repräsentation (z) statt über das Originalbild (x).

[![Technische Zeichnung des Models von Stable Diffusion @ai__pub](media/Technische_Zeichnung_des_Models_von_Stable_Diffusion_@ai__pub.jpg)](https://www.heise.de/imgs/18/3/5/9/8/6/9/6/1561362589082218496-images-0-20b84afc7440ea83.jpg)

Diagramm zu Stable Diffusion: Der Encoder komprimiert ein Bild x zu einer Repräsentation z, es folgen Diffusion und Rauschunterdrückung (Abb. 1).


Wer sich weiter in die technischen Hintergründe vertiefen möchte, findet bei arxiv.org das Paper der CompVis-Forschergruppe um Robin Rombach von der LMU München und Patrick Esser von Runway ML, die die Technik entwickelt haben ("[High-Resolution Image Synthesis with Latent Diffusion Models](https://arxiv.org/abs/2112.10752)"). Die Heidelberger und Münchner hatten das wissenschaftliche Paper im Dezember 2021 hochgeladen, online ist zurzeit die revidierte Version aus April 2022 greifbar. Die CompVis-Gruppe stellt auch ein [GitHub-Repository zu Latent Diffusion](https://github.com/CompVis/latent-diffusion) bereit, in dem sie ihr Vorgehen beim Pre-Training der augmentierten Diffusionsmodelle und den Weg zur Text-zu-Bild-Generierung samt vortrainierter Gewichte beschreibt. Darin erklären die Forscher, wie sich eigene Modelle trainieren lassen.

### Das Modell selbst testen

Wer Stable Diffusion testen will, benötigt einen Nutzerzugang zu Hugging Face Hub und ein Zugangstoken für den Code. Zunächst ist auf dem eigenen Rechner `diffusers==0.2.4` zu installieren mit folgendem Befehl: `pip install diffusers==0.2.4 transformers scipy ftfy`. Die zur benötigten Version 1-4 gehörige [Modellkarte ist bei Hugging Face hinterlegt](https://huggingface.co/CompVis/stable-diffusion-v1-4) und nach Lektüre der Lizenz abzunicken (durch Ankreuzen eines Kontrollfelds). Mit der Übergabe des Zugangstokens ist das Set-up abgeschlossen, und man kann mit der Inferenz loslegen.

Wie man an das Token gelangt und was die weiteren Schritte sind, ist ausführlich [im Blogeintrag zu Stable Diffusion erläutert](https://huggingface.co/blog/stable_diffusion). Eine Hürde könnte die Rechenpower sein, denn zum Betreiben des Modells ist GPU-Speicherplatz notwendig. Wer über weniger als 10 GByte an GPU-RAM verfügt, muss sich mit einer kleineren Version der Stable-Diffusion-Pipeline begnügen (float 16 precision statt `fp32`). In dem Fall wären beim Einrichten noch Extraschritte nötig, um den alternativen `fp16`-Branch einzubinden.

### Gemeinsames Projekt mit LAION und EleutherAI

Hinter Stable Diffusion stehen ein Team aus Forschern und Ingenieuren der Non-Profit-Organisation LAION, die Forschungsabteilung des KI-Unternehmens Stability AI sowie CompVis, eine Gruppe an der Ludwig-Maximilians-Universität München (LMU), die aus der vormaligen Computer Vision Group der Universität Heidelberg hervorgegangen ist. Stable Diffusion beruht auf vereinten Kräften der Machine-Learning-Community: So hat sich auch die Community des Graswurzelkollektivs EleutherAI eingebracht, die bereits GPT-Neo und GPT-J schuf.

LAION steht für Large-scale Artificial Intelligence Open Network und ist nicht gewinnorientiert. Das ist bemerkenswert, denn die Organisation finanziert sich (anders als Unternehmen wie Google, Meta und das mit Microsoft liierte OpenAI) ausschließlich über Spenden und öffentliche Forschungsgelder. Das Ziel von LAION ist laut Projektbeschreibung, die wesentlichen Ergebnisse aus dem hochskalierten Machine Learning zugänglich zu machen – und zwar allen, die sich dafür interessieren. Diesem Ziel soll offenbar auch Stable Diffusion dienen.

### Lesen Sie auch

[

![](media/abb15_-_Kopie.jpg-b446b1c70f62e7bb.jpeg.jpg)

### KI-System DALL·E: Ein Alleskönner für Kreative

heise Developer





](https://www.heise.de/hintergrund/KI-System-DALL-E-Ein-Alleskoenner-fuer-Kreative-7206468.html)

[

![](media/maxresdefault.jpg-fc67ae968518056c.jpeg.jpg)

### Dall-E-2 & Co: Bild-Generatoren im Test

c't Magazin





](https://www.heise.de/news/Dall-E-2-Co-Bild-Generatoren-im-Test-7221014.html)

[

![](media/dalle-bowls.jpg-7bd4a97fdac8949d.jpeg.jpg)

### Bilder mit KI erstellen: DALL-E startet kostenpflichtige Betaphase

heise Developer





](https://www.heise.de/news/Bilder-mit-KI-erstellen-DALL-E-startet-kostenpflichtige-Betpaphase-7185400.html)

[

!["An Alpaca is smiling and under water in a swimming pool." #imagen by Zoubin Ghahramani @ZoubinGhahrama1](data:image/svg+xml;base64,PD94bWwgdmVyc2lvbj0iMS4wIiBlbmNvZGluZz0iVVRGLTgiPz4KPHN2ZyB3aWR0aD0iNjk2cHgiIGhlaWdodD0iMzkxcHgiIHZpZXdCb3g9IjAgMCA2OTYgMzkxIiB2ZXJzaW9uPSIxLjEiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyIgeG1sbnM6eGxpbms9Imh0dHA6Ly93d3cudzMub3JnLzE5OTkveGxpbmsiPgogICAgPGcgc3Ryb2tlPSJub25lIiBmaWxsPSIjZjJmMmYyIiBmaWxsLW9wYWNpdHk9IjEiPgogICAgICAgIDxyZWN0IHg9IjAiIHk9IjAiIHdpZHRoPSI2OTYiIGhlaWdodD0iMzkxIj48L3JlY3Q+CiAgICA8L2c+Cjwvc3ZnPg==)

### Fotorealistische KI-Bildsynthese: Google macht DALL·E 2 Konkurrenz – mit Imagen

heise Developer





](https://www.heise.de/news/Fotorealistische-KI-Bildsynthese-Google-macht-DALL-E-2-Konkurrenz-mit-Imagen-7121826.html)

[

![](data:image/svg+xml;base64,PD94bWwgdmVyc2lvbj0iMS4wIiBlbmNvZGluZz0iVVRGLTgiPz4KPHN2ZyB3aWR0aD0iNjk2cHgiIGhlaWdodD0iMzkxcHgiIHZpZXdCb3g9IjAgMCA2OTYgMzkxIiB2ZXJzaW9uPSIxLjEiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyIgeG1sbnM6eGxpbms9Imh0dHA6Ly93d3cudzMub3JnLzE5OTkveGxpbmsiPgogICAgPGcgc3Ryb2tlPSJub25lIiBmaWxsPSIjZjJmMmYyIiBmaWxsLW9wYWNpdHk9IjEiPgogICAgICAgIDxyZWN0IHg9IjAiIHk9IjAiIHdpZHRoPSI2OTYiIGhlaWdodD0iMzkxIj48L3JlY3Q+CiAgICA8L2c+Cjwvc3ZnPg==)

### Machine Learning: KI-Modell CLIP reproduziert Vorurteile

heise Developer





](https://www.heise.de/news/Machine-Learning-KI-Modell-CLIP-reproduziert-Vorurteile-6165066.html)

Mehr anzeigen

Potenziell können Milliarden von Menschen mit dem Text-zu-Bild-Modell binnen Sekunden digitale Kunstwerke im Format von 512 x 512 Pixel erstellen, denn das Modell soll sich "auf Consumer-GPUs" (unter 10 GByte virtuelle RAM) betreiben lassen, also kein eigenes Rechenzentrum erfordern – gute Nachrichten auch für unterfinanzierte Forscher.

### Weiterführende Ressourcen zu Stable Diffusion

Details zum Release von Stable Diffusion finden sich in der Ankündigung des [Public Release im Blog von Stability AI](https://stability.ai/blog/stable-diffusion-public-release) und in einem [Blogeintrag bei Hugging Face](https://huggingface.co/blog/stable_diffusion) – dort sind auch die Gewichte, die Modellkarte und der Code hinterlegt. Die vorgelagerte Ankündigung des Forschungsrelease bietet zusätzliche Einblicke und [Stellungnahmen der Beteiligten](https://stability.ai/blog/stable-diffusion-announcement). Wer besser verstehen möchte, wie Diffusionsmodelle funktionieren, kann sich in der Diffuser-Library bei Hugging Face umsehen (Colab "[Getting started with diffusers](https://colab.research.google.com/github/huggingface/notebooks/blob/main/diffusers/diffusers_intro.ipynb)").

Auf Twitter sind bereits Erklär-Threads zu finden, unter anderem von dem Machine-Learning-Professor Tom Goldstein mit einer Übersicht relevanter Forschungsarbeiten (Thread: "[How diffusion models work](https://twitter.com/tomgoldsteincs/status/1562503814422630406), how we understand them, and why I think this understanding is broken"). Besonders empfehlenswert ist der Überblick bei AI Pub:

![](media/profile-image.jpg)**AI Pub**[@ai__pub](https://twitter.com/ai__pub)

// Stable Diffusion, Explained // You've seen the Stable Diffusion AI art all over Twitter. But how does Stable Diffusion _work_? A thread explaining diffusion models, latent space representations, and context injection: 1/15 https://t.co/VX9UVmUaKJ

[![](media/0-1.jpg)](https://api.heise.de/svc/embetty/tweet/1561362542487695360/images/0)[![](media/1.jpg)](https://api.heise.de/svc/embetty/tweet/1561362542487695360/images/1)[![](media/2-1.jpg)](https://api.heise.de/svc/embetty/tweet/1561362542487695360/images/2)[![](media/3-1.jpg)](https://api.heise.de/svc/embetty/tweet/1561362542487695360/images/3)

[21.8.2022, 16:40:13 via Twitter](https://twitter.com/ai__pub/status/1561362542487695360) [powered by](https://www.heise.de/embetty?wt_mc=link.embetty.poweredby "embetty - displaying remote content without compromising your privacy.")

Wer mit großen Bilddatensätzen arbeitet (oder es vorhat) und sich Gedanken über Copyrightfragen macht, findet eine aufschlussreiche [FAQ-Sammlung auf der Website von LAION](https://laion.ai/faq/).

([sih](mailto:sih@ix.de "Silke Hahn"))