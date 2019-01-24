### Enabling as a `systemd` service
To enable the imaging stack as a `systemd` service that starts on reboot:
```
sudo systemctl enable <path to s4s-imaging-stack.service>
```
The [main reference stack](https://github.com/sync-for-science/reference-stack-docker) must also be installed as a `systemd` service.
