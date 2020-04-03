## Directions
Install jupyterhub as described here: [https://jupyterhub.readthedocs.io/en/stable/quickstart.html](https://jupyterhub.readthedocs.io/en/stable/quickstart.html)

Make sure jupyter notebook is working, and then modify your jupyter config file as descibed here [https://github.com/jupyterhub/jupyterhub/issues/379](https://github.com/jupyterhub/jupyterhub/issues/379) with this code so embedding the iframe works. You may need to first create your config file with `jupyter notebook --generate-config`
```
c.JupyterHub.tornado_settings = { 'headers': {'Content-Security-Policy': "frame-ancestors 'http://localhost:8080'", } }
```

Lastly run `python -m SimpleHTTPServer 8080` and `jupyterhub` at once and visit [http://localhost:8080](http://localhost:8080)



