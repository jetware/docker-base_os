FROM scratch AS i1

COPY --from=jetware/base_os:alpine3.8 /bin/ /bin/
COPY --from=jetware/base_os:alpine3.8 /etc/ /etc/
COPY --from=jetware/base_os:alpine3.8 /lib/ /lib/
COPY --from=jetware/base_os:alpine3.8 /sbin/ /sbin/
COPY --from=jetware/base_os:alpine3.8 /tmp/ /tmp/
COPY --from=jetware/base_os:alpine3.8 /usr/ /usr/
COPY --from=jetware/base_os:alpine3.8 /var/ /var/

FROM scratch
COPY --from=i1 / /

COPY fetch /fetch
