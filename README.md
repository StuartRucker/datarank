c.JupyterHub.tornado_settings = {
    'headers': {
        'Content-Security-Policy': "frame-ancestors 'ec2-url:9000'",
    }
}


python -m SimpleHTTPServer 8080


