npp_tabs: 'unindent on backspace key' plugin for Notepad++
==========================================================

This is a simple hacked up Notepad++ plugin that enables 'unindent on
backspace'. I wrote it many many years ago... and even though I no
longer use Notepad++, I guess it still works?

Installation
------------

Download 'npp_tabs.dll' from the bin directory of this repository.

In modern versions of Notepad++, you can go to the "Settings"
menu, "Import", "Import Plugin(s)", and directly import the DLL
as a plugin. If that doesn't work, you can just copy it directly
to your Notepad++ plugins folder... which is usually at
C:\Program Files\Notepad++\plugins

This plugin is known to work in versions of Notepad++ since 4.x.

Backstory
---------

(Originally posted on my blog at http://www.virtualroadside.com/blog/index.php/2012/12/03/notepad-plugin-to-enable-unindent-on-backspace-key/)

When I first started using editors, I was a tabs person. I always set
the tab size to 4 since I liked the way that looked, and used tabs
instead of spaces. And it wasn't really a philosophical reason behind
it, it was very simple actually:

_I *really* hate hitting backspace 4 times to unindent_

Seems simple enough. Yes, I know you can use SHIFT-BACKSPACE or other
voodoo to make it work, but I want to hit *one* key.

Because of this, I always used 4-space tabs instead of inserting spaces
instead of tabs. However, at some point I started writing a project in
python, and python tends to encourage spaces vs tabs. Notepad++ is my
favorite editor, so I decided to write a plugin for Notepad++ to make
using spaces a lot less annoying -- and in particular, to make it so
that when I hit backspace, it would magically eat the spaces back to the
next indentation level.

In the process of trying to do this, I discovered that the Scintilla
editing component actually has this functionality built-in -- you just
need to enable SCI_SETBACKSPACEUNINDENTS on the editor component. So I
took the sample plugin for Notepad++ and added two lines of code that
enabled this functionality, and it works great! Ever since then, I've
used spaces instead of tabs, since I really can't tell the difference --
and that's how I like it :)

I actually wrote this thing a rather long time ago, and never got around
to actually cleaning it up and releasing it. I've decided to release it
in its present form, since it's so useful and very simple. It would be
even better if Notepad++ had an option to enable this, but this works
just as well until that happens.

License
-------

GPLv2+ license.