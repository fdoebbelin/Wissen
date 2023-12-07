mit pandoc HTML-Datei in Markdown umwandeln

```
pandoc -o index.md index.html
```

allen Bildreferenzen von `image` nach `_resources` ändern

alle Zeile mit Markdown-Direktiven  mit regulärem Ausdruck entfernen

```
^:::.*\n
\{.*\n.*\}
```

alle StyleSheet-Angaben entfernen

```
\{.*\}
```

entferne Zeilenbrüche in Absätzen

```
'([^ ])$\n' --> '$1 '
'([.!?:]) $' --> '$1\n'
```

weitere Formatierungen

```
'\[(.*:)\] ' --> '**$1** '
```

