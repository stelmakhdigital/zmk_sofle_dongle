# zmk_sofle_dongle

Settings `config/west.yml`

```yaml
manifest:
  remotes:
    - name: zmkfirmware
      url-base: https://github.com/zmkfirmware
    - name: stelmakhdigital
      url-base: https://github.com//stelmakhdigital
  projects:
    - name: zmk
      remote: zmkfirmware
      revision: main
      import: app/west.yml
    - name: zmk_sofle_dongle
      remote: stelmakhdigital
      revision: master
  self:
    path: config
```


Paste the shield in the `build.yaml` file:

```yaml
---
include:
  - board: nice_nano_v2
    shield: corne_dongle_pro_micro nice_view_adapter dongle_display_view_pro_micro"
```

