

.. toctree::
   :maxdepth: 2

   intro
   strings
   datatypes
   numeric
   (many more documents listed here)




.. highlight:: python

.. now all you need to do is indent and type code...






what
  Definition lists associate a term with
  a definition.

how
  The term is a one-line phrase, and the
  definition is one or more paragraphs or
  body elements, indented relative to the
  term. Blank lines are not allowed
  between term and definition.



Showing code examples
---------------------

Examples of Python source code or interactive sessions are represented using
standard reST literal blocks.  They are started by a ``::`` at the end of the
preceding paragraph and delimited by indentation.

Representing an interactive session requires including the prompts and output
along with the Python code.  No special markup is required for interactive
sessions.  After the last line of input or output presented, there should not be
an "unused" primary prompt; this is an example of what *not* to do::

    # python hopefully
    print(tom)


Syntax highlighting is done with `Pygments <http://pygments.org>`_ (if it's
installed) and handled in a smart way:



* Within Python highlighting mode, interactive sessions are recognized
  automatically and highlighted appropriately.  Normal Python code is only
  highlighted if it is parseable (so you can use Python as the default, but
  interspersed snippets of shell commands or other code blocks will not be
  highlighted as Python).



* The valid values for the highlighting language are:

  * ``none`` (no highlighting)
  * ``python`` (the default when :confval:`highlight_language` isn't set)
  * ``guess`` (let Pygments guess the lexer based on contents, only works with
    certain well-recognizable languages)
  * ``rest``
  * α 
  * α
  ``α``
  * ε
  * ``c``
  * ... and any other lexer name that Pygments supports.





.. code-block:: python

    # comment
    print(something)





.. code-block:: bash
    :caption: Code block with syntax highlighting and line numbers
    :linenos:
    :emphasize-lines: 9,10,34,39,46

    # This code block uses bash syntax highlighting
    # Also, a code-block has args for line numbers,
    # highlighting lines, and captions!







.. rubric:: Footnotes

.. [1] There is a standard ``.. include`` directive, but it raises errors if the
       file is not found.  This one only emits a warning.
