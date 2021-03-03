FROM kcollins/ignition:8.1.2

RUN sqlite3 /var/lib/ignition/data/db/home_automation.db

COPY --chown=ignition:ignition ./ignition.conf /var/lib/ignition/data/ignition.conf
COPY maggioCA.crt /usr/local/share/ignition/lib/runtime/jre-nix/lib/security/ssl_cert
RUN cd /usr/local/share/ignition/lib/runtime/jre-nix/bin \
 && ./keytool -importcert \
 -file ../lib/security/ssl_cert \
 -alias maggio_ca \
 -cacerts \
 -noprompt -storepass "changeit"
