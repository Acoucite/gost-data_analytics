FROM jupyter/base-notebook

RUN conda install --quiet --yes \
    'numpy' \
    'psycopg2'\
	'matplotlib'\
	'psycopg2'\
	'ipywidgets'\
	'python-dateutil'\
	'jupyter_contrib_nbextensions'
	
RUN jupyter nbextension enable --py widgetsnbextension --sys-prefix
