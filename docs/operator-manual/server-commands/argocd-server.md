## argocd-server

Run the ArgoCD API server

### Synopsis

The API server is a gRPC/REST server which exposes the API consumed by the Web UI, CLI, and CI/CD systems.  This command runs API server in the foreground.  It can be configured by following options.

```
argocd-server [flags]
```

### Options

```
      --address string                                Listen on given address (default "0.0.0.0")
      --app-state-cache-expiration duration           Cache expiration for app state (default 1h0m0s)
      --application-namespaces strings                List of additional namespaces where application resources can be managed in
      --as string                                     Username to impersonate for the operation
      --as-group stringArray                          Group to impersonate for the operation, this flag can be repeated to specify multiple groups.
      --as-uid string                                 UID to impersonate for the operation
      --basehref string                               Value for base href in index.html. Used if Argo CD is running behind reverse proxy under subpath different from / (default "/")
      --certificate-authority string                  Path to a cert file for the certificate authority
      --client-certificate string                     Path to a client certificate file for TLS
      --client-key string                             Path to a client key file for TLS
      --cluster string                                The name of the kubeconfig cluster to use
      --connection-status-cache-expiration duration   Cache expiration for cluster/repo connection status (default 1h0m0s)
      --content-security-policy value                 Set Content-Security-Policy header in HTTP responses to value. To disable, set to "". (default "frame-ancestors 'self';")
      --context string                                The name of the kubeconfig context to use
      --default-cache-expiration duration             Cache expiration default (default 24h0m0s)
      --dex-server string                             Dex server address (default "argocd-dex-server:5556")
      --dex-server-plaintext                          Use a plaintext client (non-TLS) to connect to dex server
      --dex-server-strict-tls                         Perform strict validation of TLS certificates when connecting to dex server
      --disable-auth                                  Disable client authentication
      --enable-gzip                                   Enable GZIP compression
      --enable-proxy-extension                        Enable Proxy Extension feature
      --gloglevel int                                 Set the glog logging level
  -h, --help                                          help for argocd-server
      --insecure                                      Run server without TLS
      --insecure-skip-tls-verify                      If true, the server's certificate will not be checked for validity. This will make your HTTPS connections insecure
      --kubeconfig string                             Path to a kube config. Only required if out-of-cluster
      --logformat string                              Set the logging format. One of: text|json (default "text")
      --login-attempts-expiration duration            Cache expiration for failed login attempts (default 24h0m0s)
      --loglevel string                               Set the logging level. One of: debug|info|warn|error (default "info")
      --metrics-address string                        Listen for metrics on given address (default "0.0.0.0")
      --metrics-port int                              Start metrics on given port (default 8083)
  -n, --namespace string                              If present, the namespace scope for this CLI request
      --oidc-cache-expiration duration                Cache expiration for OIDC state (default 3m0s)
      --otlp-address string                           OpenTelemetry collector address to send traces to
      --password string                               Password for basic authentication to the API server
      --port int                                      Listen on given port (default 8080)
      --proxy-url string                              If provided, this URL will be used to connect via proxy
      --redis string                                  Redis server hostname and port (e.g. argocd-redis:6379). 
      --redis-ca-certificate string                   Path to Redis server CA certificate (e.g. /etc/certs/redis/ca.crt). If not specified, system trusted CAs will be used for server certificate validation.
      --redis-client-certificate string               Path to Redis client certificate (e.g. /etc/certs/redis/client.crt).
      --redis-client-key string                       Path to Redis client key (e.g. /etc/certs/redis/client.crt).
      --redis-compress string                         Enable compression for data sent to Redis with the required compression algorithm. (possible values: gzip, none) (default "gzip")
      --redis-insecure-skip-tls-verify                Skip Redis server certificate validation.
      --redis-use-tls                                 Use TLS when connecting to Redis. 
      --redisdb int                                   Redis database.
      --repo-server string                            Repo server address (default "argocd-repo-server:8081")
      --repo-server-plaintext                         Use a plaintext client (non-TLS) to connect to repository server
      --repo-server-strict-tls                        Perform strict validation of TLS certificates when connecting to repo server
      --repo-server-timeout-seconds int               Repo server RPC call timeout seconds. (default 60)
      --request-timeout string                        The length of time to wait before giving up on a single server request. Non-zero values should contain a corresponding time unit (e.g. 1s, 2m, 3h). A value of zero means don't timeout requests. (default "0")
      --rootpath string                               Used if Argo CD is running behind reverse proxy under subpath different from /
      --sentinel stringArray                          Redis sentinel hostname and port (e.g. argocd-redis-ha-announce-0:6379). 
      --sentinelmaster string                         Redis sentinel master group name. (default "master")
      --server string                                 The address and port of the Kubernetes API server
      --staticassets string                           Directory path that contains additional static assets (default "/shared/app")
      --tls-server-name string                        If provided, this name will be used to validate server certificate. If this is not provided, hostname used to contact the server is used.
      --tlsciphers string                             The list of acceptable ciphers to be used when establishing TLS connections. Use 'list' to list available ciphers. (default "TLS_ECDHE_RSA_WITH_AES_256_GCM_SHA384:TLS_RSA_WITH_AES_256_GCM_SHA384")
      --tlsmaxversion string                          The maximum SSL/TLS version that is acceptable (one of: 1.0|1.1|1.2|1.3) (default "1.3")
      --tlsminversion string                          The minimum SSL/TLS version that is acceptable (one of: 1.0|1.1|1.2|1.3) (default "1.2")
      --token string                                  Bearer token for authentication to the API server
      --user string                                   The name of the kubeconfig user to use
      --username string                               Username for basic authentication to the API server
      --x-frame-options value                         Set X-Frame-Options header in HTTP responses to value. To disable, set to "". (default "sameorigin")
```

### SEE ALSO

* [argocd-server version](argocd-server_version.md)	 - Print version information

