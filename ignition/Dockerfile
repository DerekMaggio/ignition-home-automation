FROM kcollins/ignition:8.1.1

RUN apt install python2.7
RUN sqlite3 /var/lib/ignition/data/db/home_automation.db

COPY --chown=ignition:ignition ./ignition.conf /var/lib/ignition/data/ignition.conf
COPY --chown=ignition:ignition ./modules/ZWaveDriver-unsigned.modl /var/lib/ignition/user-lib/modules/ZWaveDriver-unsigned.modl
