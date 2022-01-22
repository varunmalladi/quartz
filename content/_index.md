---
title: 🖊 rooney's math notes
---
I use Obsidian to keep track of my notes, and I've ported those here. Click the search bar or type '/' to find a specific note, 
see on one of the featured notes below, or use the interactive graph at the bottom (which displays "connections" between notes, 
represented as dots).

## Featured
- [Homotopy category, nerve, and decategorification](<notes/ntpy/Key Ideas/Homotopy theory/homotopy category, nerve, and decategorification.md>)
- [Representations of sl2C](<notes/ntpy/Key Ideas/Representation theory/repreresentations of sl2C.md>)
- [Product type](<notes/ntpy/Definitions/Logic/Product type.md>)

## Bugs
The Quartz platform I'm using doesn't currently support the type of links I use in Obsidian. I've written a program which I send my 
all my notes through before uploading them here, which tries to edit them so that they are Quartz-compatible, but there are some 
bugs. Most notably,
- "gather" and "align" environments are broken, as Obsidian requires them to be surrounded by "$$" while this causes MathJax to not render them.
- Obsidian supports links to pages that have not been created yet— my program changes those links to point to the path "", which happens to be the home page. Thus the home page appears as the largest dot on the graph.
