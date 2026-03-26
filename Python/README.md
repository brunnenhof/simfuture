# Python source code

The game is coded in python using [NiceGUI](https://nicegui.io/) and extensive coding help from [Claude Sonnet](https://www.anthropic.com/claude/sonnet). Claude did most of the user interface, the state management for NiceGUI and the VPS deployment. I did the model transpiling.

The file *ugregmod.py* is the Vensim model transpiled to Python (by a php script I coded - Claude reached its limits here). It is a module called by toy.py (which is the main python file). For speed, the model is a numpy matrix with all variables horizontally and all timesteps vertically. Since a Vensim model is initially completetly defined if all values at any timestep are completely defined, the game uses horizontal slices for each round for further speed improvements. A subset of all variables is saved locally as *.npy files at the end of each round for display purposes.  

*game_plot_ug.py* is a python module (not coded by Claude) that contains all the logic to produce the results graphs, by region, role and round. It is also called by toy.py  The graphs are all matplotlib graphs, they might by more interesting, but also more busy, if coded in plotly ...

*luf.py* is the language file, currently for English, formal and informal German, French and Norwegian (bokmål). Might be extended to other languages in the future. The basic translations are done by [deepl.com](https://www.deepl.com/en) and then reviewed by native speakers.
