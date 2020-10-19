# PyData Global 2020

This folder contains the presentation about decision making with Bayesian methods
for PyData Global 2020. The presentation is created from a Jupyter notebook by using
[RISE](https://rise.readthedocs.io/en/stable/) and is then served with
[Binder](https://mybinder.org/). 

## Build slides locally
The libraries required to build the slides locally can be installed from the
requirements file:

    pip install -r requirements.txt


### Use RISE (recommended)
RISE allows to generate the slides from the Jupyter notebook editor itself
with a single click:

![rise_button](img/rise_button.png)

### Use `nbconvert`
To render slides use `jupyter nbconvert foo.ipynb --to slides --post serve`

## Serve slides for presentation
The slides are served using the environment in [arviz_sandbox](https://github.com/arviz-devs/arviz_sandbox)
for convenience and speed, see
[this post](https://discourse.jupyter.org/t/tip-speed-up-binder-launches-by-pulling-github-content-in-a-binder-link-with-nbgitpuller/922?u=oriolabril)
in Jupyter Discourse for a detailed description.

To generate the binder shield with the link to the presentations the following
steps should be followed:

* Make sure the notebook metadata has `"livereveal": {"autolaunch": true}`. If
  you create you presentation as a copy of the English one it will already be
  done.
  * This (as you'll see when editing) generates the presentation automatically
    whenever the notebook is opened. To edit the notebook close the
    presentation and modify the cells contents. More details in
    [RISE documentation](https://rise.readthedocs.io/en/stable/customize.html)
* Generate the binder link to run the notebook in the sandbox environment.
  There is a helper page [nbgitpuller link generator](https://jupyterhub.github.io/nbgitpuller/link).
  The `Binder` tab allows to specify
  * `Git Environment Repository URL`: `https://github.com/arviz-devs/arviz_sandbox`
  * `Git Content Repository URL`: `https://github.com/arviz-devs/arviz_misc`
  * and the file to be opened
* Create a custom shield from [Binder docs](https://mybinder.readthedocs.io/en/latest/howto/badges.html)
