# openresty-brotli

Example dockerfile of adding Brotli to Openresty nginx. Forked from [openresty debian example](https://github.com/openresty/docker-openresty/blob/master/archive/Dockerfile.jessie).

Mainly these two lines, since openresty is identical to nginx:

```
&& git clone --recursive https://github.com/google/ngx_brotli \
&& ./configure -j${RESTY_J} ${_RESTY_CONFIG_DEPS} ${RESTY_CONFIG_OPTIONS} ${RESTY_CONFIG_OPTIONS_MORE} --add-module=ngx_brotli \
```