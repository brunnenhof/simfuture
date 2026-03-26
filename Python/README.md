# Python source code

The game is coded in python using [NiceGUI](https://nicegui.io/) and extensive coding help from [Claude Sonnet](https://www.anthropic.com/claude/sonnet). Claude did most of the user interface, the state management for NiceGUI and the VPS deployment. I did the model transpiling.

The file *ugregmod.py* is the Vensim model transpiled to Python (by a php script I coded - Claude reached his limits here). It is a module called by toy.py (which is the main python file).
