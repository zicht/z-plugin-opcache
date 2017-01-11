# `opcache` plugin for zicht/z

Clears the opcache after deploy.

## Example:

```yml
plugins: ['env', 'opcache']

envs:
    production:
        ssh: user@production
        root: ~/site
        web: web
        http: 'http://example.org'
```

Running `z env:opcache --explain` would show you that a file is put on the
remote containing code to clear the cache, and that file is retrieved using
curl.

The `env:opcache` task is also hooked into `deploy.post`

# Maintainer(s)
* Gerard van Helden <gerard@zicht.nl>
