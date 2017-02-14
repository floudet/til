# sudo Preserve Environment 

Say you want to execute a command with elevated privileges, but keep your environment variables (`http_proxy` for instance).

`sudo` offers this feature through its `-E` option:

```
-E          The -E (preserve environment) option indicates to the security policy that the user wishes to preserve their
            existing environment variables.  The security policy may return an error if the -E option is specified and the
            user does not have permission to preserve the environment.
```

