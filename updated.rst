

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
  * python 
  * ``python`` (the default when :confval:`highlight_language` isn't set)
  * ``guess`` (let Pygments guess the lexer based on contents, only works with
    certain well-recognizable languages)
  * ``rest``
  * α  -  more information 
  * α 
  * ε 
  * ``c`` 






.. code-block:: python

 class TD3(object):
    def __init__(
      self,
      state_dim,
      action_dim,
      max_action,
      discount=0.99,
      tau=0.005,
      policy_noise=0.2,
      noise_clip=0.5,
      policy_freq=2
    ):

      self.actor = Actor(state_dim, action_dim, max_action).to(device)
      self.actor_target = copy.deepcopy(self.actor)
      self.actor_optimizer = torch.optim.Adam(self.actor.parameters(), lr=3e-4)

      self.critic = Critic(state_dim, action_dim).to(device)
      self.critic_target = copy.deepcopy(self.critic)
      self.critic_optimizer = torch.optim.Adam(self.critic.parameters(), lr=3e-4)
      self.α  =  'tom'
      self.max_action = max_action
      self.discount = discount
      self.tau = tau
      self.policy_noise = policy_noise
      self.noise_clip = noise_clip
      self.policy_freq = policy_freq

      self.total_it = 0








.. code-block:: python

    # comment
    print(something)







.. rubric:: Footnotes

.. [1] There is a standard ``.. include`` directive, but it raises errors if the
       file is not found.  This one only emits a warning.
