## Komando für das Script 1
mkdir /volume1/docker/paperless-ngx && \
mkdir /volume1/docker/paperless-ngx/redisdata && \
mkdir /volume1/docker/paperless-ngx/data && \
mkdir /volume1/docker/paperless-ngx/media && \
mkdir /volume1/docker/paperless-ngx/export && \
mkdir /volume1/docker/paperless-ngx/consume

## Komando für das Script 2 (kopieren)
find /volume1/incoming-scans/ -type f -mmin -62 -exec rsync -a --no-relative {} /volume1/docker/paperless-ngx/consume/ \; > /dev/null 2>&1
