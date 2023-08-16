Apple introduced AppleScript very early as a language to automate the operating system and programs. Therefore, there is a considerable amount of information available on AppleScript, although much of it is a bit aged now.

Many people consider AppleScript to be a “simple” language that is “easy to learn”. While it may look like this on the surface, I disagree with this assessment. AppleScript is verbose and requires a lot of typing. It *is* easy to understand for native English speakers because it uses simple English sentences like `set this to that` or `get the first item of (records as list)`. This may seem obvious to native speakers, but it is more difficult for speakers of other languages since the vocabulary is vast and sometimes obscure.

Furthermore, Apple stopped the development of its scripting language long ago. It is sorely missing basic string functions, regular expressions, array methods, and so on.

JavaScript, on the other hand, is terse, sometimes to the point of being unintelligible. It provides all the functions one would expect of a modern programming language. You use `this=that` to set a value and `list[0]` to get the first element of a list. The vocabulary is limited, and therefore easy to learn. Also, JavaScript is available in every browser today and on the desktop (in the form of npm). It is used by far more people, in far more projects, and on far more projects than AppleScript.

But almost all problems can be solved in any programming language. So if you prefer AppleScript, stick with it, by all means.

## Short History [#](#short-history)

JavaScript for Automation (JXA) has been introduced by Apple with macOS 10.10. It should allow automating software on macOS with a second, modern scripting language. However, the work on it was never really finished, and Apple seems to have abandoned any development on JXA. Although you can use it for automation, you occasionally must work around rough edges or take a detour to achieve the same functionality as in AppleScript. And some things are not possible at all, although they should be, according to the documentation.

## Structure of this site [#](#structure-of-this-site)

You should read the following chapters before diving into scripting proper:

- [Introduction to JXA](https://bru6.de/jxa/introduction-to-jxa/) gives you a short overview of the main tools and techniques to write, run and debug JXA scripts
- [Basics](https://bru6.de/jxa/jxa-basics/) introduces some recurring concepts that you’ll need in most of your scripts.
    - [A first example](https://bru6.de/jxa/basics/a-first-example/) shows a simple example of a JXA script.
    - [Working with Objects](https://bru6.de/jxa/basics/working-with-objects/) explains the general approach to handle objects in JXA, how to use their properties etc.
    - [Working with Apps](https://bru6.de/jxa/basics/working-with-apps/) explains how to work with applications, in particular how to get information about their properties, elements and methods.
    - [Limitations](https://bru6.de/jxa/basics/limitations/) highlights some of the things you *can not* do with JXA. You should check it out if you have some experience with JavaScript programming for web projects.

After that, you may head over to [Automating Applications](https://bru6.de/jxa/automating-applications/). There you’ll find more in-depth examples for working with different programs like Mail, Notes, Contacts, and others.

Whenever you see an underlined reference to a code line, the line will be highlighted in the corresponding code block when you mouse over it.