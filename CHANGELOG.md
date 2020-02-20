
# Changelog

## 1.9.12

- Prometheus port changed in `pkg/deploy/assets/assets.go` from 9091 to 656
- GitHook port change in `pps/server/githook/githook.go` from 999 to 655
- Bump etcd version from v3.3.5 to v3.3.18 for stability of SQS spout jobs executing 1000 
  times per minutes filling up the etcd volume
