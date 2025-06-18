# Managing services and packages on Synology NAS (DSM 7.2+) via terminal

### Terminal command to manage services:

/usr/syno/bin/synosystemctl (_run as root or add sudo to beginning of command_)

#### Usage

/usr/syno/bin/synosystemctl {COMMAND}

#### Commands

#### start \[--no-block] NAME... Start (activate) one or more units stop \[--no-block] NAME... Stop (deactivate) one or more units enable NAME... Enable one or more unit files disable NAME... Disable one or more unit files restart \[--no-block] NAME... Start or restart one or more units try-restart \[--no-block] NAME... Restart one or more units if active reload \[--no-block] NAME... Reload one or more units reload-or-restart \[--no-block] NAME... Reload or restart one or more units reenable NAME... Reenable one or more unit files isolate \[--no-block] NAME... Start one unit and stop all others mask \[--runtime] NAME... Mask one or more units unmask \[--runtime] NAME... Unmask one or more units uninstall NAME Remove units from system, as well as relating symlinks and flags daemon-reload Reload unit config get-default Get the name of the default target set-default NAME Set the default target get-enable-status NAME Get the enable status of given unit get-active-status NAME Get the active status of given unit get-load-status NAME Get the load status of given unit stop-service-by-reason REASON NAME... Stop one or more services by a reason start-service-by-reason REASON NAME... Start one or more services by a reason remove-service-reason REASON NAME... Remove reason for one or more services list-service-reason NAME List service reason get-unit-by-pid PID Get unit name that the pid belongs to list-service-by-mnt-path PATH List services using given mount path register-volume NAME VOLUME Register a volume for a unit package-register-volume NAME VOLUME Register a volume for a package unregister-volume NAME VOLUME Unregister a volume for a unit package-unregister-volume NAME VOLUME Unregister a volume for a package
